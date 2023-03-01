## Lazy Loading :

```
Lazy loading is one of the most common design patterns used in web and mobile development. 
It is widely used with frameworks like Angular and React to increase an application’s performance by reducing initial loading time.
```

```
In simple terms, lazy loading is a design pattern. 
It allows you to load parts of your application on-demand to reduce the initial load time. 
For example, you can initially load the components and modules related to user login and registration. 
Then, you can load the rest of the components based on user navigation.
```

```
You might not feel much difference when using lazy loading for small-scale applications. 
But it significantly impacts large-scale applications by reducing the initial load time. 
Ultimately, it improves both the user experience and the application’s performance.
```

#### Advantages of Lazy Loading
- Reduces initial loading time by reducing the bundle size.
- Reduces browser workload.
- Improves application performance in low bandwidth situations.
- Improves user experience at initial loading.
- Optimizes resource usage.

#### Disadvantages of Lazy Loading
- Not suitable for small-scale applications.
- Placeholders can slow down quick scrolling.
- Requires additional communication with the server to fetch resources.
- Can affect SEO and ranking.


## Code:
```
// Without React.lazy()
import AboutComponent from './AboutComponent ';

// With React.lazy()
const AboutComponent = React.lazy(() => import('./AboutComponent '));

const HomeComponent = () => (
    <div><AboutComponent /></div>
)
```

## React.Suspense:

- When we use lazy loading, components are rendered as we navigate. 
- So, we need to have a placeholder for those components until they are loaded. 
- As a solution, React.Suspense was introduced, and it acts as a wrapper for the lazy components.
- You can wrap a single lazy component, multiple lazy components, or multiple lazy components with different hierarchy levels with React.Suspense. 
- In addition, it accepts a prop named fallback as the placeholder, and you can pass a component or an element for that.

For example, you can pass the waiting or loading message as the fallback prop, and it will be displayed until the wrapped lazy component is rendered.

```
import React, { Suspense } from "react";
const AboutComponent = React.lazy(() => import('./AboutComponent'));

const HomeComponent = () => (
    <div><Suspense fallback = { <div> Please Wait... </div> } >
            <AboutComponent /></Suspense></div>
);
```

```
As you can see, you need to use both the React.lazy() and React.Suspense features to build a lazy-loading component in React. 
These features are straightforward and anyone with basic React knowledge can easily use them.
```

## Memory Leak:
```
A Memory leak is a commonly faced issue when developing React applications. 
A memory leak is a type of **resource leak** that occurs when an application incorrectly manages memory allocations. 
That memory, which is not needed anymore, is not released for other processes to use. 
A memory leak may also happen when an object is stored in a memory, but cannot be accessed by the running code.
```

## Why should you clean up memory leaks?
```
Memory leaks are commonly faced issues when developing React applications. 
```

### It causes many problems, including:

- Affecting the project’s performance by reducing the amount of available memory;
- Slowing down the application;
- Refreshing the page randomly;
- Crashing the system;
- Overloading database with huge amounts of queries;

## What causes a memory leak?

```
A memory leak appears when React applications created subscriptions that were made when a component was mounted and
did not unsubscribe them when those components were unmounted.
```
### These subscriptions could be:

- DOM Event listeners;
- WebSocket subscriptions;
- Requests to an API;

## How to clean up memory leaks?
```
Modern programming languages and frameworks have techniques for clearing out data that is no longer needed. And react is not an exception.
```

Basically, we need to remove subscriptions when the component unmounts. For that there are three ways:

1. Clearing Intervals
```
You may use setInterval function for creating repeating tasks every second or so. This will likely result in a memory leak error and it must be cleared after unmounting.
```

## Code

```
 useEffect(() => {
    let isMounted = true;
    
    const interval = setInterval(() => {
      if (isMounted) {
        getData(cookiesList);
      }
    }, 5000);

    return () => {
      isMounted = false;
      clearInterval(interval);
    };
  });
```

## How to detect memory leaks?
```
There is a way to detect memory leaks before you get the error from react. Simply use google chrome’s developers tools. 
Go to Memory tab take heap snapshots and do a comparison between times before you took an action
```

## Error Boundaries:
 ```
 Error Boundaries basically provide some sort of boundaries or checks on errors, 
 They are React components that are used to handle JavaScript errors in their child component tree.
 ```
 
 ## Pure Function:
 ```
 A React component is considered pure if it renders the same output for the same state and props. 
 For this type of class component, React provides the PureComponent base class.
```
- Its return value is only determined by its input values
- Its return value is always the same for the same input values

## Code:
```
import React from 'react';

class PercentageStat extends React.PureComponent {

  render() {
    const { label, score = 0, total = Math.max(1, score) } = this.props;

    return (
      <div>
        <h6>{ label }</h6>
        <span>{ Math.round(score / total * 100) }%</span>
      </div>
    )
  }

}

export default PercentageStat;
```

## HOC component:
```
Higher-order components or HOC is the advanced method of reusing the component functionality logic. 
It simply takes the original component and returns the enhanced component.
```

## Syntax:
`const EnhancedComponent = higherOrderComponent(OriginalComponent);`

## Reason to use Higher-Order component:

- Easy to handle
- Get rid of copying the same logic in every component
- Makes code more readable

## Parent Component 
```
import React from 'react'
import "./App.css"
// importing HighOrder file
import EnhancedComponent from './HighOrder'

class App extends React.Component {
render() {
	// Destructuring the props
	const { show, handleclick } = this.props

	// Calling out the props
	return <button onClick={handleclick}>{show}
	</button>
}
}


export default EnhancedComponent(App);

```

## Child Component 
```
import React from 'react'

const EnhancedComponent = (OriginalComponent) => {
	class NewComponent extends React.Component {

		constructor(props) {
			super(props);
			// Set initial count to be 0
			this.state = { count: 0 };
		}

		handleClick = () => {
			// Incrementing the count
			this.setState({ count: this.state.count + 1 });
		}

		render() {

			// passed a handleclick and count in the originalComponent
			// as a props for calling and adding the functionality
			return <OriginalComponent
				handleclick={this.handleClick}
				show={this.state.count} />
		}
	}
	// Returns the new component
	return NewComponent
}
// Export main Component
export default EnhancedComponent

```
## Output:
<img src="https://media.geeksforgeeks.org/wp-content/cdn-uploads/20210310121357/20210310_121315.gif" />






