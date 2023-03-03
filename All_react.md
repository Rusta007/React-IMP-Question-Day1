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










