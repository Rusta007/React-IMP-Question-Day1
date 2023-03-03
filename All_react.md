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

## State vs Props

| State | Props |
| :---- | :---- |
| State can be changed. | Props are read-only. |
| States is mutable. | Props are immutable. |
| State holds info about the components. | Props allow you to pass data from one component to other component as as argument. |
| State cannot be accepted by **child component** . | Props can be accessed by the **child component** .|
| State can be used for rendering dynamic changes with the components. | Props are used to communicate between two components. |
| State cannot make components reusable. | Props can make components to re-usable. |

## Pass Props Parent to Child Component 

![Screenshot 2023-02-27 162940](https://user-images.githubusercontent.com/94469107/221546758-a25898ef-666f-4137-abcf-9422c4ee96bc.png)

## Pass Props Child to Parent Component 

![Screenshot 2023-02-27 164459](https://user-images.githubusercontent.com/94469107/221549637-b6863545-de2f-4c2f-9d39-99aed2e28ecc.png)

## Update State

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












