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

## Class Component 

![Screenshot 2023-03-13 155111](https://user-images.githubusercontent.com/94469107/224674330-b800c75c-577e-4e19-86f1-b8f8836ce348.png)

## Function Component 

![Screenshot 2023-03-13 160222](https://user-images.githubusercontent.com/94469107/224676799-93a5cefa-be66-4e4b-9370-738a5e9584a7.png)


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

## State | Update State

#### Code

![Screenshot 2023-02-27 165338](https://user-images.githubusercontent.com/94469107/221551565-8f1b51f4-1854-4450-a517-4f098dfeace5.png)

#### Output

![update-state-on-props-change](https://user-images.githubusercontent.com/94469107/221552208-0d1cb97b-a641-4b8a-98ca-60e334978f2a.gif)


