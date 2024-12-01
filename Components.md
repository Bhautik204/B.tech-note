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


---

## Component in File
- React is recommended to split your components into separate files.
- To do that, create a new file with a .js extension and put component code inside that file.
- **Note:** the file name as well as class/function name MUST start with capital letter.
- We also need to export that function class from the created file using **default export keywords,** for example:
Welcome.js
```js
function Welcome() {
  return (
    <h1> Hello World from other file</h1>
  );
}

export default Welcome;
```

index.js
```js
import Welcome from './Welcome';

const root = //create root code here;
root.render(<Welcome />);
```

#REACT