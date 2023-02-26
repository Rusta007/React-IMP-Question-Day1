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










