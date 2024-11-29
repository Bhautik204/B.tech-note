## Introduction
- JS library for building User Interface(UI). It lets you compose complex UIs from small and isolated pieces of code called **"component"**.
- It is used to create **Single Page Application(SPA)**.
- fronted framework created by **Facebook(Meta)**.
- Create virtual DOM in memory , instead of manipulating browser's DOM directly.
- It change in virtual DOM First and then it will reflect change in browser's DOM.
- React will find what changes have been made and changes only what needs to be changed.

---
## Setup a Environment
- https://codesandbox.io to write/run React code directly using browser without any pre-requisite.
- to install react in local system , need Node.js and npm after installing npm use npx command to install/setup new react app using below cmd. 
`npx create-react-app my-app`
- to run react app need to start using npm cmd.
`cd my-app
`npm start`

---

## JSX
```JS
root.render(<h1> hello world</h1>)
```
- consider above line of code, notice argument passed in render method, this weird tag syntax is neither string nor HTML, its called **JSX**.
- **JSX** stand for ***JavaScript XML***.
- JSX allows to write HTML in React, It makes it easier to write and add HTML in React.
- We can also embed expression in JSX using curly braces, for example
```JS
const root = ReactDOM.crateRoot(document.getElementByID('root'));
const name = "Bhautik Godhasara"
root.render(<h1>hello from { name }</h1>)
```

---

## Components
- Components split the UI into independent, reusable pieces, and think about each piece in isolation.
- components are like JavaScript functions. They accept arbitrary inputs (**called “props”**) and return React elements describing what should appear on the screen.
- Components are independent and reusable bits of code. They serve the same purpose as *JavaScript functions*, but work in isolation and *return HTML*.
- ***Components come in two types***, **Class components** and **Function components.**
- When creating a React component, the component's name **MUST** start with an **upper case letter**.

---

## Function Components 
 - most preferred component for development 
- simplest way to define a component is to write a JavaScript function:
```JS
function Welcome() {
    return <h1>Hello world</h1>;
}
root.render(<Welcome/>);
```
or ES6 function
```JS
const Welcome = ()=>{
    return(<h1>Hello World</h1>);
}
root.render(<Welcome/>);
```
- We can also use *props (properties)* with the Function component, for example
```JS
function Welcome(props){
    return <h1>Hello world from { props.name }</h1>
}
root.render(<Welcome name="Bhautik" />);
```
- This function is a valid React component because it accepts a single “props” (which stands for properties) object argument with data and returns a React element. 
- We call such components **“function components”** because they are literally JavaScript functions.

---

## Class Components
- A class component must include the extends **React.Component** statement.
- This statement creates an inheritance to React.Component, and gives your component access to React.Component's functions.
- The component also requires a render() method, this method returns HTML.
```JS
class Welcome extends React.Component {
    render(){
        return(<h1>Hello world</h1>);
    }
}
root.render(<Welcome/>);
```
- Similar to function component we can have properties in class components as well, we can directly access properties in class component with the help of built-in object named props.
```JS
class Welcome extends React.Component {
    render(){
        return(<h1>Hello world from {this.props.name}</h1>);
    }
}
```