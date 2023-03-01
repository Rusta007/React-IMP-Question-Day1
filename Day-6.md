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
As you can see, you need to use both the React.lazy() and React.Suspense features to build a lazy-loading component in React. 
These features are straightforward and anyone with basic React knowledge can easily use them.
```








