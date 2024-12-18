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

## [[Components]]
- Components split the UI into independent, reusable pieces, and think about each piece in isolation.
- components are like JavaScript functions. They accept arbitrary inputs (**called “props”**) and return React elements describing what should appear on the screen.
- Components are independent and reusable bits of code. They serve the same purpose as *JavaScript functions*, but work in isolation and *return HTML*.
- ***Components come in two types***, **Class components** and **Function components.**
- When creating a React component, the component's name **MUST** start with an **upper case letter**.

---
## Events
- Handling events with React elements is very similar to handling events on DOM elements. There are some syntax differences:
	- React events are named using camelCase, rather than lowercase.
	- With JSX you pass a function as the event handler, rather than a string.
For HTML:
```HTML
<button onclick="activateLasers()">
  Activate Lasers
</button>
```

JSX:
```js
<button onClick={activateLasers}>
  Activate Lasers
</button>
```
- Note that in JSX we can use all events from Java Script just have to name it in camelCase, ex. onClick, onDblClick, onChange etc…
- To pass argument with the events we can use arrow function syntax, for example:
```JS
<button onClick={()=>activateLasers(parameters)}>
  Activate Lasers
</button>
```

---

## [[Routing]]

#REACT 