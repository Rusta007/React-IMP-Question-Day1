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





