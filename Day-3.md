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



