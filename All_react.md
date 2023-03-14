# Day1

## React Introduction 
```bash
React is a Free, Open-source, Frontend-JS Library.
It's used to build User-Interface and Single-Page-Application, and it is component-based.
It's developed by JORDAN WALKE, and maintained by Facebook.
```
## React Features
### React uses many things, that's why it became easy and powerful.

1. JSX
```
  JSX is Javascript Syntax Extension.
  JSX provides us to write HTML in JS file.
  JSX is not provided by the Browser, basically It work like complier to transform in Echma-Script, Where **Babel** and **Webpack** are used.
```

2. Virtual-Dom
```
A virtual DOM object is a representation of the original DOM object. 
Whenever any modifications happen in the web application, the entire UI is re-rendered in virtual DOM representation. 
Then it checks the difference between the previous DOM representation and new DOM, this difference between them known as Diffing Algorithm.  
Once it has done, the real DOM will update only the things that have actually changed. This makes the application faster, and there is no wastage of memory.
```
![what-is-dom-in-react2](https://user-images.githubusercontent.com/94469107/221536238-7a9fb497-c505-4202-809b-36b342063e1c.jpg)


4. Components 
 ```
 A Component is one of the core building blocks of React. 
 In other words, we can say that every application you will develop in React will be made up of pieces called components. 
 Components make the task of building UIs much easier. 
 You can see a UI broken down into multiple individual pieces called components and work on them independently and merge them all in a parent component which will be     your final UI. 
 Components in React basically return a piece of JSX code that tells what should be rendered on the screen. 
 In React, we mainly have two types of components: 
 ```
4. SPA (Single Page Application)
```
A single page application, the webpage does not reload the page during its runtime and instead works within a browser. 
```
5. SEO (Search Engine Optimization) Friendly 
```
Search Engine Optimization (SEO) is the process of optimizing your website in order to improve its visibility and ranking on search engines such as Google, Bing, and Yahoo.
```
6. Community Support 
7. Build Web & Mobile Application 
8. React Dev Tools
9. Easy learning Curve ~

## Library vs Framework

| Library   | Framework|
| :-------- | :------- |
| A library implements a particular function. | a framework as a collection of libraries  |
| Our code controls when and where to call a library. | The Framework controls calling of librariesfor our code. |
| Helps us to reuse a software function. | Helps us to developa software application quickly. |
| Intent of a libraryis to provide reusable software functionality. | Intent of a framework is to reduce the complexity of the software development process. |
| **Examples** :  React, JQuery | **Examples** : AngularJS, NodeJS, Spring |

## Bable Vs Webpack

| Babel | Webpack |
| :-----| :-------|
| Babel is a very famous `Transpiler`. It convert latest version code of JS, in that language or code which understandable by the Browser. | Webpack is a popular `module bundling system` built on the top of Browser or Node.js, and It Takes all the JS files and other assets, transforming them into one `Large-File`. |
| Babel is simply a translator, who translates your 'fancy' (ES6+) JS code into 'not-so-fancy' (ES5) ones that browser (front-end) or Node.js (back-end) understands. | Webpack as a mega-multi-translator that works with all kinds of languages (or assets).  |
| we need Babel to translate **ES6-code** into the equivalent not-so-fancy code **ES5-code** , that our browser or Node.js actually understands. | **For example**, Webpack often runs Babel as one of its jobs. Another example, Webpack can collect all your inline CSS styles in your Javascript files (.EXE) and bundle them into one.  |

### What is Transpiler?
```
  Transpiler is convert code into source-to-source code at a same level.
  It means we have lower level just like:- Binary code, but
  Transpiler covert at a same level of code into which is browser can understand.
  Without Worrying we can use latest version of code in our browser, the code will work or not. 
```
## NPM vs NPX

| NPM | NPX |
| :-- | :-- |
| NPM is Node Package Manager | NPX is Node Package Execute. |
| It's used to install, uninstall & update JS package on your machine. | It's used to execute JS package directly, without installing them. |
| NPM installed packages globally, which means that your machine may be polluted by packages.  | NPX doesn't install packages, so packages pollution on the machine isn't a concern. |


## Class Component vs Functional Component

| Class Component | Function Component |
| :-------------- | :----------------- |
| A Class Component required to extend from React.Component. Create a render function which returns a React Element. | A Function Component is just plain JS code. that accepts props as an argument & returns a React Element(**JSX**). |
| It must have the render method to return JSX Element. | There is no Render method to used in functional Component. |
| Class component use Lifecycle method, It's kept alive & invoked depending on phase of class component. | Functional Component run the code from Top to Bottom and once the function is returned it, it can be kept alive. |
| Class Component is known as Stateful component, Because it implement logic and state. | Function Component is known as Stateless component, because it only accepts data or state and display them in some Form. |
| Lifecycle method can be used inside class component. | React lifecycle method cannot be used in the function component. |
| It cannot use Hooks. | Function Component uses Hooks, Using Hooks we can make out state as **Stateful component** . |
| Class Component used constructor to pass props. | Function Component doesn't need it.  |

#### Example of Class Component:

![Screenshot 2023-03-13 155111](https://user-images.githubusercontent.com/94469107/224685210-f9f50c4a-38b3-4a80-8a35-597fcaa4206e.png)

- Summary of code:
```
In this example, MyComponent is a class that extends the Component class from the React library. It has a constructor that sets the initial state of the component, which includes a count property that starts at 0. It also has a handleClick method that updates the component's state when the button is clicked, and a render method that returns the component's HTML markup.

When the button is clicked, the handleClick method is called, which updates the state of the component by incrementing the count property. This causes the component to re-render, which updates the displayed count value.
```
#### Example of Function Component:

![Screenshot 2023-03-13 160222](https://user-images.githubusercontent.com/94469107/224685305-fc7e105f-2bd3-4cbd-aaaa-a5797ab3ae3e.png)

- Summary of code:

```
In this example, MyComponent is a function that returns the component's HTML markup. It uses the useState hook from React to create a state variable called count and a function to update it called setCount. The initial value of count is set to 0.

When the button is clicked, the handleClick function is called, which updates the count state variable by calling setCount. This causes the component to re-render, which updates the displayed count value.
```

## State vs Props

| State | Props |
| :---- | :---- |
| State can be changed. | Props are read-only. |
| States is mutable. | Props are immutable. |
| State holds info about the components. | Props allow you to pass data from one component to other component as as argument. |
| State cannot be accepted by **child component** . | Props can be accessed by the **child component** .|
| State can be used for rendering dynamic changes with the components. | Props are used to communicate between two components. |
| State cannot make components reusable. | Props can make components to re-usable. |

#### Example of State:

![Screenshot 2023-03-13 165113](https://user-images.githubusercontent.com/94469107/224687732-89283e05-5128-46e9-9149-d84c651c3568.png)

- Summary of code:
```
In this example, the useState hook is used to create a state variable called count and a function to update it called setCount. The initial value of count is set to 0.

When the button is clicked, the handleClick function is called, which updates the count state variable by calling setCount. This causes the component to re-render, which updates the displayed count value.
```

#### Example of Props:

Child Component 

![Screenshot 2023-03-13 165335](https://user-images.githubusercontent.com/94469107/224688277-102fa61b-4893-41e8-809e-1d9396372f66.png)


Parent Component 

![Screenshot 2023-03-13 165357](https://user-images.githubusercontent.com/94469107/224688296-b4934698-b0c9-424b-9955-576d3cb6b3bb.png)

- Summary of code:
```
In this example, the Greeting component takes in two props: name and age. These props are passed in as arguments to the component function via the props object.

The component uses the props to display a personalized greeting with the person's name and age. The name prop is used inside an <h1> tag, while the age prop is used inside a <p> tag.

To use this component elsewhere in the application, it would be imported and rendered with the desired props:

```


## Pass Props Parent to Child Component 

![Screenshot 2023-02-27 162940](https://user-images.githubusercontent.com/94469107/221546758-a25898ef-666f-4137-abcf-9422c4ee96bc.png)

## Pass Props Child to Parent Component 

![Screenshot 2023-02-27 164459](https://user-images.githubusercontent.com/94469107/221549637-b6863545-de2f-4c2f-9d39-99aed2e28ecc.png)

## State | Update State

#### Code

![Screenshot 2023-02-27 165338](https://user-images.githubusercontent.com/94469107/221551565-8f1b51f4-1854-4450-a517-4f098dfeace5.png)

#### Output

![update-state-on-props-change](https://user-images.githubusercontent.com/94469107/221552208-0d1cb97b-a641-4b8a-98ca-60e334978f2a.gif)



# Day-2

## Conditional Rendering in Function and Class Component
```
Conditional rendering is a term to describe the ability to render different user interface (UI) markup if a condition is true or false. 
In React, it allows us to render different elements or components based on a condition. 
```
#### There are many concepts:
1. if...else....
2. Ternary Operators 
3. Logical && Operator

## If... else
```
it is the simple conditional rendering statement implemented in render method. 
This if-else statement is worked in a 2-way process. 
2-way process is like if one block of code does not satisfy the given condition, it will go to other block of code.  
If the given condition is true, it returns the block of code present in “if” else it returns the block of code present in “else”.    
```
#### Syntax

![Screenshot 2023-02-26 204319](https://user-images.githubusercontent.com/94469107/221419273-e4f86967-5991-43f6-ab42-7c302330dff0.png)


### Code
![page1](https://user-images.githubusercontent.com/94469107/221418792-c1f83743-e460-442c-957b-f79e2896564c.png)

# Ternary Operators 
```
This operator is used in the situations, where we have two blocks of code each other on a given condition. 
This operator is as like the “if-else” statement. 
This ternary operator is used as the short form notation for if-else, and it is written in a single line. 
It takes 3 operands and returns the output according to it.
```

#### Syntax
```
condition ? true : false 
```
###### If the condition is true, the 1st statement will be rendered, else the 2nd one would render
### Code

![Screenshot 2023-02-26 210024](https://user-images.githubusercontent.com/94469107/221420197-bdeb0979-6115-478c-8d41-168ce9155b8c.png)

# Logical && Operator
```
&& is a boolean operator, which essentially means “and”. For the condition to evaluate to true, both of the statements must be individually true.
```
#### Syntax 
```
{ condition && <Component/> }
```
### Code

![Screenshot 2023-02-26 214843](https://user-images.githubusercontent.com/94469107/221422646-854a0c4a-3c30-4ba5-a81c-2026e1396612.png)

# Lifecycle 
```
Lifecycle methods are series of events that happen throughout the birth, growth, and death of a React component.
```

1. Mounting (adding nodes to the DOM)
2. Updating (altering existing nodes in the DOM)
3. Unmounting (removing nodes from the DOM)

## Mounting (adding nodes to the DOM)
```
The Mounting phase refers to the phase during which a component is created and inserted to the DOM.
```
#### There are many methods but only Three methods are important:

1. constructor()
```
The Constructor() method is called with the props, as arguments, and you should always start by calling the super(props) before anything else, 
this will initiate the parent's constructor method and allows the component to inherit methods from its parent (React.Component).
```
2. render()
```
The render() method is required, and is the method that actually outputs the HTML to the DOM.
```
3. componentDidMount()
```
This function is invoked immediately after the component is mounted to the DOM.
You would use the componentDidMount lifecycle method to grab a DOM node from the component tree immediately after it’s mounted.
```
### Code

![Screenshot 2023-02-26 225940](https://user-images.githubusercontent.com/94469107/221426409-818f55da-abaf-417c-8948-8d5fcc8b332e.png)

## Updating (altering existing nodes in the DOM)
```
Whenever a change is made to the state or props of a React component, the component is rerendered.
In simple terms, the component is updated. This is the updating phase of the React component lifecycle.
```
1. componentDidUpdate()
```
The componentDidUpdate method is called after the component is updated in the DOM.
```
![Screenshot 2023-02-26 230627](https://user-images.githubusercontent.com/94469107/221426717-80dd9a5a-9027-4014-b0a1-ff24b65cc86a.png)

## Unmounting (removing nodes from the DOM)
```
React has only one built-in method that gets called when a component is unmounted.
```
1. componentWillUnmount()
```
The componentWillUnmount lifecycle method is invoked immediately before a component is unmounted and destroyed.
```
![Screenshot 2023-02-26 235509](https://user-images.githubusercontent.com/94469107/221429265-2002acb7-5790-4485-a4f2-a5149e6c7c43.png)

### Day-3

# Hooks

### What is Props-Drilling?
```
Prop drilling is basically a situation when the same data is being sent at almost every level due to requirements in the final level.
Passing data through multiple components is not a good way of writing clean, reusable, and DRY code.
```
#### Example:

<img src="https://lh5.googleusercontent.com/K1veBT9r_aQPq_iYI9MdtljbsBu8egv7n8cu78fWqzL0POVn2xb66r_gEFgJ8qg9FxphsGFqNZIDQ3QZ0zuT-XtEcrpNVZylXvxhDTPAySL8_FJWiIGHlcXggcHYCFKaQeNp8HRQvCZZQHRULaf8_vtg8mgyZElVhkSiUYgicFQ0mo6zPgGve9-Pcg" width="500" height ="500"/>

### Props-Drilling Code
```
import React, { useState } from "react";

function Parent() {
const [fName, setfName] = useState("firstName");
const [lName, setlName] = useState("LastName");
return (
	<>
	<div>This is a Parent component</div>
	<br />
	<ChildA fName={fName} lName={lName} />
	</>
);
}

function ChildA({ fName, lName }) {
return (
	<>
	This is ChildA Component.
	<br />
	<ChildB fName={fName} lName={lName} />
	</>
);
}

function ChildB({ fName, lName }) {
return (
	<>
	This is ChildB Component.
	<br />
	<ChildC fName={fName} lName={lName} />
	</>
);
}

function ChildC({ fName, lName }) {
return (
	<>
	This is ChildC component.
	<br />
	<h3> Data from Parent component is as follows:</h3>
	<h4>{fName}</h4>
	<h4>{lName}</h4>
	</>
);
}

export default Parent;

```

## Solution of Props-Drilling:
```
The React context API is a fast way of avoiding prop drilling and ensuring your data is managed globally.
```

### What is Context API??
```
React context is a built-in API that uses the useContext hook to share data across components.
Imagine passing the data of an authenticated user from a parent component to a deep nested child component. This will be cumbersome if you need to pass the data through a lot of intermediate components.

A better approach to doing this is using React context to handle the data.  
```

### How to Use the React Context API??
```
useContext is a built-in hook in React. You can start using the context API by importing the **createContext** function from React.
```

#### Step-1: createContext
#### we initialized our context and named it globalContext.
```
Import {createContext} from ‘react’;

const globalContext = createContext();
```

#### Step-2: provide the context
#### The context API uses a provider to pass data to its child components. You will have to wrap all components with a provider component.
```
<globalContext.Provider value={...}> // Like BrowserRouter
	<ParentComponent/>
<globalContext.Provider>
```

#### Example:
```
import React from ‘react’;

function App() {

	const username = “John Doe”
    
	return(
        <globalContext.Provider value={username}> 
        	<Dashboard/>
        <globalContext.Provider>
    )
}

export default App;
```

## There are two ways to consume the context.
` Way-1 `

#### Step-3: Consume the context 
```
We can consume the context by using the useContext hook.
Without passing data through nested components, you can access your context in any component you want. 
```

```
import { useContext } from ‘react’;

const Profile = () => {

	const value = useContext(globalContext);  //Consume the context way-1
    
	return (
        <div>
        	{value}                         // used state directly where we want
        </div>
    )
}

export default Profile
```
` Way-2 `
```
import { globalContext } from './context';  // Import your globalContext.

function ChildComponent() {
  return (
    <globalContext.Consumer>
      {value => <span>{value}</span>}
    </globalContext.Consumer>
  );
}
```

#### Example of useContext
 <img src="https://dmitripavlutin.com/90649ae4bdf379c482ad24e0dd220bc4/react-context-3.svg" />
 
 
# useState:
```
The useState() is a Hook that allows you to have state variables in functional components.
It returns an array with two values: **the current state** and a **function to update** it. 
The Hook takes an initial state value as an argument and returns an updated state value whenever the setter function is called.
useState is a named export from react. To use it, you can write React.useState or import it by writing useState:
```

### Syntax:
` const [state, setState] = useState(initialValue); `

```
the **initialValue** is the value you want to start with, and **state** is the current state value that can be used in your component. 
The **setState function** can be used to update the state, triggering a re-render of your component.
```

### Updating objects:
```
const [state, setState] = useState({ name: 'John', age: 30 });

const updateName = () => {
  setState({ ...state, name: 'Jane' });
};

const updateAge = () => {
  setState({ ...state, age: state.age + 1 });
};

```

### Updating Array:
```
const [array, setArray] = useState([1, 2, 3, 4, 5]);

const addItem = () => {
  setArray([...array, 6]);
};

const removeItem = () => {
  setArray(array.slice(0, array.length - 1));
};
```

## Code with Array:
```
const MessageList = () => {
  const [message, setMessage] = useState("");
  const [messageList, setMessageList] = useState([]);

  return (
    <div>
      <input
        type="text"
        value={message}
        placeholder="Enter a message"
        onChange={e => {
          setMessage(e.target.value);
        }}
      />
      <input
        type="button"
        value="Add"
        onClick={e => {
          setMessageList([
            ...messageList,
            {
              // Use the current size as ID (needed to iterate the list later)
              id: messageList.length + 1,
              message: message
            }
          ]);
          setMessage(""); // Clear the text box
        }}
      />
      <ul>
        {messageList.map(m => (
          <li key={m.id}>{m.message}</li>
        ))}
      </ul>
    </div>
  );
};
```

# useEffect:
```
In useEffect, The word effect refers to a functional programming term called a "side effect".
**Side-Effects**
1. tasks like updating the DOM
2. fetching data from API end-points
3. setting up subscriptions or timers
```

## Why do we need useEffect:
```
if we wanted to change the title meta tag to display the user's name in their browser tab, 
we could do it within the component itself, but we shouldn't.
```
```
function User({ name }) {
  document.title = name; 
  // This is a side effect. Don't do this in the component body!
    
  return <h1>{name}</h1>;   
} 
```

## How do I use useEffect?
```
import { useEffect } from 'react';

function User({ name }) {
  useEffect(() => {
    document.title = name;
  }, [name]);
    
  return <h1>{name}</h1>;   
}
```
- The function passed to useEffect is a callback function. This will be called after the component renders.

- In this function, we can perform our side effects or multiple side effects if we want.

- The second argument is an array, called the dependencies array. This array should include all of the values that our side effect relies upon.

## Dependencies

1. **No dependency passed:**
-  useEffect runs after every render without the dependencies array, causing infinite loop

2. **An empty array:**
- Runs only on the first render

3. **Props or state values:**
- Runs on the first render
- And any time any dependency value changes
- you can add multiple values by separating them by commas

## Code 

![Screenshot 2023-02-28 145946](https://user-images.githubusercontent.com/94469107/221811103-7e163ef9-8791-4eba-a6c3-a6518c7686dd.png)

# useMemo:
```
The useMemo is a hook used in the functional component of react that returns a memoized value.

**Memoized value**
- In Computer Science, memoization is a concept used in general when we don’t need to recompute the function with a 
  given argument for the next time as it returns the cached result. 
 - A memoized function remembers the results of output for a given set of inputs.

**Situation:**
- if there is a function to add two numbers, and we give the parameter as 1 and 2 for the first time the function will add these two numbers and return 3, 
- but if the same inputs come again then we will return the cached value i.e 3 and not compute with the add function again. 

```

#### Syntax:
```
const memoizedValue = useMemo(functionThatReturnsValue, arrayDepencies)
```

#### Code:

![Screenshot 2023-02-28 151250](https://user-images.githubusercontent.com/94469107/221814663-640451e5-b18c-4160-8980-27218731ea05.png)

### WithMemo Output:-
- Now in the above example, we have used the user memo hook, here the function that returns the value
-  i.e squareNum is passed inside the useMemo and inside the array dependencies, 
-  we have used the number as the squareNum will run only when the number changes. 
-  If we increase the counter and the number remains the same in the input field the squareNum doesn’t run again

# useReducer:
```
The useReducer Hook is the better alternative to the useState hook and is generally more preferred over the useState hook 
when you have complex state-building logic or when the next state value depends upon its previous value or when the components are needed to be optimized.
```
### Syntax:
```
const [state, dispatch] = useReducer(reducer, initialArgs, init);

- The useReducer hook takes three arguments including reducer, initial state, and the function to load the initial state lazily.
```
### Example: 

![Screenshot 2023-02-28 152035](https://user-images.githubusercontent.com/94469107/221816492-dee00e3b-d38d-4b58-8f5b-55450d1d2cf9.png)

### Output:
<img src="https://media.geeksforgeeks.org/wp-content/uploads/20201103231033/gfg.gif" />

# useCallback:
```
The useCallback hook is used when you have a component in which the child is rerendering again and again without need.
- Pass an inline callback and an array of dependencies. 
- useCallback will return a memoized version of the callback that only changes if one of the dependencies has changed. 
- This is useful when passing callbacks to optimized child components that rely on reference equality to prevent unnecessary renders.
```

### Syntax:
```
const memoizedCallback = useCallback(
 () => {
   doSomething(a, b);
 },
 [a, b],
);
```
### Code:

![Screenshot 2023-02-28 153244](https://user-images.githubusercontent.com/94469107/221820749-096aaf65-3778-4ac4-85b0-cef03ed45916.png)

# useRef
```
The useRef is a hook that allows to directly create a reference to the DOM element in the functional component. 
```

### Syntax:
```
const refContainer = useRef(initialValue);
```
- The useRef returns a mutable ref object. This object has a property called .current. 
- The value is persisted in the refContainer.current property. 
- These values are accessed from the current property of the returned object. 
- The .current property could be initialised to the passed argument initialValue e.g. useRef(initialValue). 
- The object can persist a value for a full lifetime of the component. 

### Code:

```
import React, {Fragment, useRef} from 'react';

function App() {

// Creating a ref object using useRef hook
const focusPoint = useRef(null);
const onClickHandler = () => {
	focusPoint.current.value =
	"The quick brown fox jumps over the lazy dog";
	focusPoint.current.focus();
};
return (
	<Fragment>
	<div>
		<button onClick={onClickHandler}>
		ACTION
		</button>
	</div>
	<label>
	Click on the action button to
	focus and populate the text.
	</label><br/>
	<textarea ref={focusPoint} />
	</Fragment>
);
};

export default App;

```

## useState vs useReducer

- useState and useReducer are both hooks in React that allow you to manage state within your components. However, there are a few key differences between them:

- **State management**: useState manages state in a single value or object, while useReducer manages state with a more complex data structure.

- **Complex state updates**: useState is suitable for managing simple state updates, such as toggling a boolean or updating a single value. useReducer is better for managing complex state updates that involve multiple values and may require conditional logic.

- **Performance** : useReducer may be more performant in certain cases, especially when the state updates are complex and involve many values. This is because useReducer allows you to dispatch an action that triggers a state update, which can be more efficient than updating state directly with useState.

- **Predictability** : useReducer promotes predictability in state updates by following a strict pattern of taking in a previous state and an action to update that state. This can make it easier to understand how state is being updated and debug issues.

- **Debugging**: useReducer can be easier to debug since state updates are triggered by dispatching an action, which can be logged and traced.

```
In summary, useState is a simpler and more straightforward way of managing state, while useReducer is better for managing complex state updates that require more conditional logic and may be more performant in certain cases.
```

## useMemo vs useCallback

- useMemo and useCallback are both hooks in React that allow you to optimize the performance of your application by memoizing values or functions.

- useMemo is used to memoize a value that is expensive to compute, so that it is only computed when necessary. 
- It takes two arguments: a function that computes the 	value, and an array of dependencies. 
- The value returned by the function is memoized and only recomputed when the dependencies change. 

#### Here's an example:

```
const memoizedValue = useMemo(() => {
  return someExpensiveComputation(a, b);
}, [a, b]);

- In this example, someExpensiveComputation is only called when a or b change.
```

- useCallback is used to memoize a function, so that it is only recreated when necessary. 
- It takes two arguments: a function and an array of dependencies. 
- The function returned by useCallback is memoized and only recreated when the dependencies change.

```
const memoizedFunction = useCallback(() => {
  doSomethingWith(a, b);
}, [a, b]);

- In this example, memoizedFunction is only recreated when a or b change.
```

The main difference between useMemo and useCallback is what they memoize. useMemo memoizes a value, while useCallback memoizes a function. In general, you should use useMemo when you want to memoize a value, and useCallback when you want to memoize a function.

However, there are cases where you might want to use useCallback to memoize a value, or useMemo to memoize a function. For example, if you have a function that returns a new function every time it is called, you might want to memoize the returned function with useCallback. Or, if you have a value that is expensive to compute and also used as a function, you might want to memoize it with useMemo.

## Day-4

## Stylig with Material UI
- Material UI is an open-source React component library that implements Google's Material Design. 
- It includes a comprehensive collection of prebuilt components that are ready for use in production right out of the box.

#### Installing Material UI
`$ npm install @material-ui/core @material-ui/icons`

## Button

![Screenshot 2023-03-01 124609](https://user-images.githubusercontent.com/94469107/222069903-d2103370-83ea-47cb-a7a6-8264bdb10b84.png)

## ColorPicker

![Screenshot 2023-03-01 124819](https://user-images.githubusercontent.com/94469107/222070287-61f0fd15-a016-4906-b53b-9753abe9390a.png)

# Form

## useState + Form

```
import React, { useState } from 'react';

const MyFormm = () => {
  const [name, setName] = useState('');
  const [email, setEmail] = useState('');
  const [message, setMessage] = useState('');

  const handleSubmit = (event) => {
    event.preventDefault();
    console.log(`Name: ${name}, Email: ${email}, Message: ${message}`);
  };

  return (
    <form onSubmit={handleSubmit}>
      <label>
        Name:
        <input type="text" value={name} onChange={(event) => setName(event.target.value)} />
      </label>
      <br />
      <label>
        Email:
        <input type="email" value={email} onChange={(event) => setEmail(event.target.value)} />
      </label>
      <br />
      <label>
        Message:
        <textarea value={message} onChange={(event) => setMessage(event.target.value)} />
      </label>
      <br />
      <button type="submit">Submit</button>
    </form>
  );
};

export default MyFormm;

```
### Summary of code:

In this example, useState is used to create state variables for the name, email, and message inputs in the form. The value prop of each input is set to the corresponding state variable, and the onChange prop is set to a function that updates the state variable with the new value of the input.

The handleSubmit function is called when the form is submitted, and logs the values of the state variables to the console. You can modify this function to handle the form data in your own application.

## useEffect + Form

```
import React, { useState, useEffect } from 'react';

const MyFormmm = () => {
  const [name, setName] = useState('');
  const [email, setEmail] = useState('');
  const [message, setMessage] = useState('');

  useEffect(() => {
    // Load initial data for the form here
    // For example, you could fetch the data from an API and set the state variables
  }, []);

  const handleSubmit = (event) => {
    event.preventDefault();
    console.log(`Name: ${name}, Email: ${email}, Message: ${message}`);
    // Reset form here
    setName('');
    setEmail('');
    setMessage('');
  };

  return (
    <form onSubmit={handleSubmit}>
      <label>
        Name:
        <input type="text" value={name} onChange={(event) => setName(event.target.value)} />
      </label>
      <br />
      <label>
        Email:
        <input type="email" value={email} onChange={(event) => setEmail(event.target.value)} />
      </label>
      <br />
      <label>
        Message:
        <textarea value={message} onChange={(event) => setMessage(event.target.value)} />
      </label>
      <br />
      <button type="submit">Submit</button>
    </form>
  );
};

export default MyFormmm;
```
### Summary of code:

In this example, useEffect is used to load initial data for the form. The useEffect hook takes two arguments: a function that will run when the component mounts, and an array of dependencies that determines when the effect should run. In this case, the dependencies array is empty, so the effect will only run once when the component mounts.

The handleSubmit function is called when the form is submitted, and logs the values of the state variables to the console. You can modify this function to handle the form data in your own application. In this example, the form is reset by setting the state variables back to their initial empty values after the form is submitted.


## useContext + Form

```
import React, { useState, useContext } from 'react';
import MyContext from './MyContext';

const UseContextForm = () => {
  const [name, setName] = useState('');
  const [email, setEmail] = useState('');
  const [message, setMessage] = useState('');
  const { submitForm } = useContext(MyContext);

  const handleSubmit = (event) => {
    event.preventDefault();
    console.log(`Name: ${name}, Email: ${email}, Message: ${message}`);
    // Pass form data to context here
    submitForm(name, email, message);
    // Reset form here
    setName('');
    setEmail('');
    setMessage('');
  };

  return (
    <form onSubmit={handleSubmit}>
      <label>
        Name:
        <input type="text" value={name} onChange={(event) => setName(event.target.value)} />
      </label>
      <br />
      <label>
        Email:
        <input type="email" value={email} onChange={(event) => setEmail(event.target.value)} />
      </label>
      <br />
      <label>
        Message:
        <textarea value={message} onChange={(event) => setMessage(event.target.value)} />
      </label>
      <br />
      <button type="submit">Submit</button>
    </form>
  );
};

export default UseContextForm;
```

### Summary of code:

In this example, useContext is used to access a submitForm function from a context object. The context object is created using the createContext function and exported as MyContext from a separate file. The submitForm function can be defined in the same file as the context object, and it should handle the form data in your own application.

The handleSubmit function is called when the form is submitted, and logs the values of the state variables to the console. The form data is then passed to the submitForm function from the context object. In this example, the form is reset by setting the state variables back to their initial empty values after the form is submitted.

## useReducer + Form

```
import React, { useReducer } from 'react';

const initialState = {
  name: '',
  email: '',
  message: '',
};

const formReducer = (state, action) => {
  switch (action.type) {
    case 'updateName':
      return { ...state, name: action.payload };
    case 'updateEmail':
      return { ...state, email: action.payload };
    case 'updateMessage':
      return { ...state, message: action.payload };
    case 'reset':
      return initialState;
    default:
      return state;
  }
};

const UseReducer = () => {
  const [state, dispatch] = useReducer(formReducer, initialState);

  const handleSubmit = (event) => {
    event.preventDefault();
    console.log(`Name: ${state.name}, Email: ${state.email}, Message: ${state.message}`);
    // Reset form here
    dispatch({ type: 'reset' });
  };

  return (
    <form onSubmit={handleSubmit}>
      <label>
        Name:
        <input type="text" value={state.name} onChange={(event) => dispatch({ type: 'updateName', payload: event.target.value })} />
      </label>
      <br />
      <label>
        Email:
        <input type="email" value={state.email} onChange={(event) => dispatch({ type: 'updateEmail', payload: event.target.value })} />
      </label>
      <br />
      <label>
        Message:
        <textarea value={state.message} onChange={(event) => dispatch({ type: 'updateMessage', payload: event.target.value })} />
      </label>
      <br />
      <button type="submit">Submit</button>
    </form>
  );
};

export default UseReducer;
```

### Summary of code: 

 In this example, useReducer is used to manage the state of the form. The initial state is defined as an object with name, email, and message properties. A formReducer function is defined to handle state updates based on different actions.

 The handleSubmit function is called when the form is submitted, and logs the values of the state variables to the console. The form is reset by dispatching a reset action to the reducer.

 The form input fields are rendered using the current state of the form, and the dispatch function is used to update the state based on user input. The dispatch function takes an action object with a type property that corresponds to a specific case in the formReducer function, and a payload property that contains the new value for the corresponding form field.


## useRef + Form

```
import React, { useRef } from 'react';

const MyForm = () => {
  const nameRef = useRef(null);
  const emailRef = useRef(null);
  const messageRef = useRef(null);

  const handleSubmit = (event) => {
    event.preventDefault();
    console.log(`Name: ${nameRef.current.value}, Email: ${emailRef.current.value}, Message: ${messageRef.current.value}`);
    // Reset form here
    nameRef.current.value = '';
    emailRef.current.value = '';
    messageRef.current.value = '';
  };

  return (
    <form onSubmit={handleSubmit}>
      <label>
        Name:
        <input type="text" ref={nameRef} />
      </label>
      <br />
      <label>
        Email:
        <input type="email" ref={emailRef} />
      </label>
      <br />
      <label>
        Message:
        <textarea ref={messageRef} />
      </label>
      <br />
      <button type="submit">Submit</button>
    </form>
  );
};

export default MyForm;

```

### Summary of code:

In this example, useRef is used to create a reference to each form input field. The nameRef, emailRef, and messageRef variables are created using the useRef hook, and assigned to the ref attribute of their respective input fields.

The handleSubmit function is called when the form is submitted, and logs the values of the form input fields to the console. The form is reset by setting the value property of each input field to an empty string.

Using useRef in this way allows you to access the current value of a form input field without the need to manage state for each field. This can be especially useful for larger forms with many input fields.

## useMemo + Form

```
import React, { useState, useMemo } from 'react';

const MyForm = () => {
  const [name, setName] = useState('');
  const [email, setEmail] = useState('');
  const [message, setMessage] = useState('');

  const handleSubmit = (event) => {
    event.preventDefault();
    console.log(`Name: ${name}, Email: ${email}, Message: ${message}`);
    // Reset form here
    setName('');
    setEmail('');
    setMessage('');
  };

  const disabled = useMemo(() => {
    return !name || !email || !message;
  }, [name, email, message]);

  return (
    <form onSubmit={handleSubmit}>
      <label>
        Name:
        <input type="text" value={name} onChange={(event) => setName(event.target.value)} />
      </label>
      <br />
      <label>
        Email:
        <input type="email" value={email} onChange={(event) => setEmail(event.target.value)} />
      </label>
      <br />
      <label>
        Message:
        <textarea value={message} onChange={(event) => setMessage(event.target.value)} />
      </label>
      <br />
      <button type="submit" disabled={disabled}>Submit</button>
    </form>
  );
};

export default MyForm;

```

### Summary of code:

In this example, useMemo is used to calculate the value of the disabled variable based on the current values of name, email, and message. The useMemo hook takes a function that returns the computed value, and an array of dependencies that trigger the recalculation of the computed value when they change.

The handleSubmit function is called when the form is submitted, and logs the values of the name, email, and message state variables to the console. The form is reset by setting the name, email, and message state variables to empty strings.

The form input fields are rendered using the current values of the name, email, and message state variables, and the setName, setEmail, and setMessage functions are used to update the state variables based on user input.

Using useMemo in this way allows you to calculate a value based on the current state of the form without triggering unnecessary re-renders. This can be especially useful for complex calculations or for optimizing performance in larger forms.

## useCallback + Form

```
import React, { useState, useCallback } from 'react';

const MyForm = () => {
  const [name, setName] = useState('');
  const [email, setEmail] = useState('');
  const [message, setMessage] = useState('');

  const handleSubmit = useCallback((event) => {
    event.preventDefault();
    console.log(`Name: ${name}, Email: ${email}, Message: ${message}`);
    // Reset form here
    setName('');
    setEmail('');
    setMessage('');
  }, [name, email, message]);

  return (
    <form onSubmit={handleSubmit}>
      <label>
        Name:
        <input type="text" value={name} onChange={(event) => setName(event.target.value)} />
      </label>
      <br />
      <label>
        Email:
        <input type="email" value={email} onChange={(event) => setEmail(event.target.value)} />
      </label>
      <br />
      <label>
        Message:
        <textarea value={message} onChange={(event) => setMessage(event.target.value)} />
      </label>
      <br />
      <button type="submit">Submit</button>
    </form>
  );
};

export default MyForm;

```

In this example, useCallback is used to create a memoized version of the handleSubmit function. The useCallback hook takes a function and an array of dependencies, and returns a memoized version of the function that only changes when one of the dependencies changes.

The handleSubmit function is called when the form is submitted, and logs the values of the name, email, and message state variables to the console. The form is reset by setting the name, email, and message state variables to empty strings.

The form input fields are rendered using the current values of the name, email, and message state variables, and the setName, setEmail, and setMessage functions are used to update the state variables based on user input.

Using useCallback in this way allows you to create a memoized version of a function that depends on state variables, and avoid unnecessary re-renders or other side effects. This can be especially useful for optimizing performance in larger forms or for complex computations that depend on state variables.


## Day-5

# React Router

- React Router is a JavaScript framework that lets us handle client and server-side routing in React applications. 
- It enables the creation of single-page web or mobile apps that allow navigating without refreshing the page.
- It also allows us to use browser history features while preserving the right application view.
- Routing is a process in which a user is directed to different pages based on their action or request.
- ReactJS Router is mainly used for developing Single Page Web Applications. 
- React Router is used to define multiple routes in the application.
- When a user types a specific URL into the browser, and if this URL path matches any 'route' inside the router file, the user will be redirected to that particular route.

## React Router Installation
`$ npm install react-router-dom --save   `

### Adding React Router Components:
1. **BrowserRouter** : 
    - BrowserRouter is a router implementation that uses the HTML5 history API(pushState, replaceState and the popstate event) to keep your UI in sync with the URL. 
    - It is the parent component that is used to store all of the other components.
2. **Routes** :
    - It’s a new component introduced in the v6 and a upgrade of the component. 
    #### The main advantages of Routes over Switch are:
    - Routes are chosen based on the best match instead of being traversed in order.
3. **Route** :
     - Route is the conditionally shown component that renders some UI when its path matches the current URL.
4. **Link** :
    - Link component is used to create links to different routes and implement navigation around the application. 
    - It works like HTML anchor tag.

## Code

```
import React, { Component } from 'react';
import { BrowserRouter as Router,Routes, Route, Link } from 'react-router-dom';
import Home from './component/home';
import About from './component/about';
import Contact from './component/contact';
import './App.css';

class App extends Component {
render() {
	return (
	<Router>
		<div className="App">
			<ul className="App-header">
			<li>
				<Link to="/">Home</Link>
			</li>
			<li>
				<Link to="/about">About Us</Link>
			</li>
			<li>
				<Link to="/contact">Contact Us</Link>
			</li>
			</ul>
		<Routes>
				<Route exact path='/' element={< Home />}></Route>
				<Route exact path='/about' element={< About />}></Route>
				<Route exact path='/contact' element={< Contact />}></Route>
		</Routes>
		</div>
	</Router>
);
}
}

export default App;
```

## Outlet

```
An <Outlet> should be used in parent route elements to render their child route elements. 
This allows nested UI to show up when child routes are rendered. 
If the parent route matched exactly, it will render a child index route or nothing if there is no index route.
```

## Code:
```
import {
  BrowserRouter,
  Routes,
  Route,
  Link,
  Outlet
} from 'react-router-dom';

function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="users" element={<Users />}>
          <Route path="/" element={<UsersIndex />} />
          <Route path=":id" element={<UserProfile />} />
          <Route path="me" element={<OwnUserProfile />} />
        </Route>
      </Routes>
    </BrowserRouter>
  );
}

function Users() {
  return (
    <div>
      <nav>
        <Link to="me">My Profile</Link>
      </nav>

      <Outlet />
    </div>
  );
}
```
## Day-6

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
import React, { PureComponent } from 'react';

class MyComponent extends PureComponent {
  render() {
    const { name } = this.props;
    return (
      <div>
        <h1>Hello, {name}!</h1>
      </div>
    );
  }
}

export default MyComponent;

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

## Day-7

# API (Application Programming Interface)

```
API is an abbreviation for Application Programming Interface which is a collection of communication protocols and subroutines 
used by various programs to communicate between them.
A programmer can make use of various API tools to make its program easier and simpler. 
Also, an API facilitates the programmers with an efficient way to develop their software programs.
```

## How we fetch the data from API 

## Using Fetch Method:

```
import React from "react";
import './App.css';
class App extends React.Component {

	// Constructor
	constructor(props) {
		super(props);

		this.state = {
			items: [],
			DataisLoaded: false
		};
	}

	// ComponentDidMount is used to
	// execute the code
	componentDidMount() {
		fetch(
"https://jsonplaceholder.typicode.com/users")
			.then((res) => res.json())
			.then((json) => {
				this.setState({
					items: json,
					DataisLoaded: true
				});
			})
	}
	render() {
		const { DataisLoaded, items } = this.state;
		if (!DataisLoaded) return <div>
			<h1> Pleses wait some time.... </h1> </div> ;

		return (
		<div className = "App">
			<h1> Fetch data from an api in react </h1> {
				items.map((item) => (
				<ol key = { item.id } >
					User_Name: { item.username },
					Full_Name: { item.name },
					User_Email: { item.email }
					</ol>
				))
			}
		</div>
	);
}
}

export default App;
```

## Output:

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20210817165343/out.gif" />


## Fetch API using async/await:

```
import React, { useState, useEffect } from 'react'
import axios from 'axios';

function App() {

	const [loading, setLoading] = useState(false);
	const [posts, setPosts] = useState([]);

	useEffect(() => {
		const loadPost = async () => {

			// Till the data is fetch using API
			// the Loading page will show.
			setLoading(true);

			// Await make wait until that
			// promise settles and return its result
			const response = await axios.get(
			"https://jsonplaceholder.typicode.com/posts/");

			// After fetching data stored it in posts state.
			setPosts(response.data);

			// Closed the loading page
			setLoading(false);
		}

		// Call the function
		loadPost();
	}, []);

	return (
		<>
			<div className="App">
				{loading ? (
					<h4>Loading...</h4>) :
					(posts.map((item) =>
						// Presently we only fetch
						// title from the API
						<h4>{item.title}</h4>)
					)
				}
			</div>
		</>
	);
}

export default App;

```

## Day-8

# REDUX

## What is Redux??
```
Redux is an open-source JavaScript library used to manage application state. 
React uses Redux for building the user interface. 
It was first introduced by **Dan Abramov and Andrew Clark** in 2015.
It allows React components to read data from a Redux Store, and dispatch Actions to the Store to update data.
Redux helps apps to scale by providing a sensible way to manage state through a unidirectional data flow model.
React Redux is conceptually simple. It subscribes to the Redux store, checks to see if the data which your component wants have changed, and re-renders your component.
```

## Redux Architecture:

<img src = "https://static.javatpoint.com/tutorial/reactjs/images/react-redux-architecture.png" />
  
1. Store:  
```
A Store is a place where the entire state of your application lists. 
It manages the status of the application and has a dispatch(action) function.
It is like a brain responsible for all moving parts in Redux.
```
2. ACTION:
```
Action is sent or dispatched from the view which are payloads that can be read by Reducers. 
It is a pure object created to store the information of the user's event. 
It includes information such as type of action, time of occurrence, location of occurrence, its coordinates, and which state it aims to change.
```
3. REDUCER:
```
Reducer read the payloads from the actions and then updates the store via the state accordingly. 
It is a pure function to return a new state from the initial state.
```

### Redux Installation:
`$ npm install redux react-redux --save  `

## Redux Toolkit:
```
Redux Toolkit makes it easier to write good Redux applications and speeds up development, by baking in our recommended best practices, 
providing good default behaviors, catching mistakes, and allowing you to write simpler code. 
  
Redux Toolkit is beneficial to all Redux users regardless of skill level or experience
```
### it helps to solve three major problems people had with Redux:

1. “Configuring a Redux store is too complicated”
2. “I have to add a lot of packages to get Redux to do anything useful”
3. “Redux requires too much boilerplate code”

## Installing Module:

`  npm install @reduxjs/toolkit  `

# Step-1:
## Store Creation:
```
Create a file called store.js by using the configureStore method from the redux toolkit package, 
pass in the list reducer’s required for the application to initialize a store.
```
## Code:

```
import { configureStore } from '@reduxjs/toolkit'
  
export const store = configureStore({
    reducer: {},
})
```

# Step-2:
### Providing Store to React application: 
```
Once the store is created, we can provide the store to the react app using the Provider method from the react-redux package.
```
### Code:
```
import ReactDOM from 'react-dom';
import { Provider } from 'react-redux';
import App from './App';
import { store } from './store.js';
  
ReactDOM.render(
  <Provider store={store}>
    <App />
  </Provider>,
  document.getElementById('root'),
);
```
# Step-3:
### Creating A Redux Slice: 

```
Create a slice.js file. In Redux Toolkit, we create a reducer using createSlice API from the redux toolkit package. 
It simplifies the creation of actions and the complex switch cases of a reducer into a few lines of code by internally using them.
```
### Code:
```
import { createSlice } from '@reduxjs/toolkit';
  
const initialState = {
  name: [],
  food: [],
};
  
const customerSlice = createSlice({
  
  // An unique name of a slice
  name: 'customer',
  
  // Initial state value of the reducer
  initialState,
  
  // Reducer methods
  reducers: {
    addCustomer: (state, { payload }) => {
      state.name.push(payload);
    },
  
    orderFood: (state, { payload }) => {
      state.food.push(payload);
    },
  },
});
  
// Action creators for each reducer method
export const { addCustomer, orderFood }
            = customerSlice.actions;
              
export default customerSlice.reducer;
```

```
Even though the above code, we use to push it doesn’t mutate the state value, since Redux toolkit uses immer library internally to update the state immutably.

Now, we import the reducer into the store.js file we created earlier. By defining a field inside the reducer parameter, we tell the store to use this slice reducer function to handle all updates to that state.
```

### Store.js
```
import { configureStore } from '@reduxjs/toolkit';
import reducer from './slice.js';
  
export default configureStore({
  reducer: {
    customers: reducer,
  },
});
```

## Using Redux state and actions in Components: 
```
We can use the react-redux hooks (useSelectore and useDispatch) to read the redux store values and dispatch actions to the reducers.
```

## Code:
```
import React, { useState } from 'react';
import { useDispatch, useSelector } from 'react-redux';
import { orderFood } from './slice.js';
  
function CustomerCard({ name }) {
  const [orders, setOrders] = useState('');
  
  // Using useSelector hook we obtain the redux store value
  const food = useSelector((state) => state.customers.food);
  
  const dispatch = useDispatch();
  
  // Using the useDispatch hook to send payload back to redux
  const addOrder = () => dispatch(orderFood(orders));
  
  return (
    <div>
      <div className="customer-food-card-container">
        <p>{name}</p>
  
        <div className="customer-foods-container">
          {food.map((foo) => (
            <div className="customer-food">{foo}</div>
          ))}
  
          <div className="customer-food-input-container">
            <input value={orders} onChange={(event) => 
              setOrders(event.target.value)} />
  
            <button onClick={addOrder}>Add</button>
          </div>
        </div>
      </div>
    </div>
  );
}
  
export default CustomerCard;
```

# Redux Thunk:

#### What is Redux Thunk??
```
Thunk is a logical concept in programming where you deal with a function that is primarily used to delay the calculation or evaluation of any operation.

Redux Thunk acts as a middleware that will return you a function instead of an object while calling through the action creators.
```

## Installation:
`  $ npm install redux thunk@2.3.0    `


### Code:
```
import { connect } from 'react-redux';  
import { addTodo } from '../actions';  
Import NewTickTackToe from '../components/NewTickTackToe';   // Another Component 
  
const DispatchToProps = dispatch => {  
  return {  
    onAddTickTackToe: ticktacktoe => {  
      dispatch(addTickTackToe(ticktacktoe));  
    }  
  };  
};  
  
export default connect(  
  null,  
  DispatchToProps  
)  
(NewTickTackToe);  
```

```
const INCREMENT_COUNTER = 'INCREMENT_COUNTER';  
  
function increment() {  
  return {  
    type: INCREMENT_COUNTER  
  };  
}  
  
function incrementAsync() {  
  return dispatch => {  
    setTimeout(() => {  
      
      dispatch(increment());  
    }, 1000);  
  };  
}  
```

### Note: The dispatch action can be used along with the increment function defined above along with time constraints. We have taken 1000 milliseconds as the default time interval. Also, the dispatch function is invoked using sync or async actions.

## Redux Saga:

```
Redux Saga is a middleware library used to allow a Redux store to interact with resources outside of itself asynchronously. 
This includes making HTTP requests to external services, accessing browser storage, and executing I/O operations. 
These operations are also known as side effects. Redux Saga helps to organize these side effects in a way that is easier to manage.
  
Redux-Saga is a library primarily aimed to make application side effects like asynchronous data fetching and accessing impure browser cache. 
It is very easy to manage and efficient to execute. With Redux-Saga, it is easy to test and handle failure effortlessly.
```

## Redux vs Context API:

<img src="https://cdn-blog.scalablepath.com/uploads/2022/08/comparison-context-api-vs-redux.webp" />



















































