### Functional Component
A functional component is a JavaScript function that may accept props as input and returns JSX that describes the user interface. It can also use React Hooks to manage state and other React features.

Basic Syntax
```javascript
function App() {
    return <h1>Hello World</h1>;
}

export default App;
```
or using an arrow function:
```javascript
const App = () => {
    return <h1>Hello World</h1>;
};

export default App;
```
Both are functional components.

### Functional Component vs Normal JavaScript Function
Normal Function
```javascript
function add(a, b) {
    return a + b;
}
```
Returns:
Number  

Functional Component
```javascript
function App() {
    return <h1>Hello</h1>;
}
```
Returns:

JSX

React takes that JSX and renders it into the DOM.

## Functional Component vs Class Component

| Functional Component | Class Component |
|----------------------|-----------------|
| JavaScript function | ES6 class |
| Returns JSX directly | Returns JSX from `render()` |
| Uses Hooks | Uses lifecycle methods and `this.state` |
| No `this` keyword | Uses `this` |
| State is managed using `useState()` | State is managed using `this.state` and `this.setState()` |
| Uses `useEffect()` for lifecycle-related behavior | Uses lifecycle methods like `componentDidMount()`, `componentDidUpdate()`, and `componentWillUnmount()` |
| Simpler and less boilerplate | More verbose and requires more boilerplate |
| Recommended for modern React development | Mostly used in legacy React applications |
