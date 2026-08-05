### JSX
JSX (JavaScript XML) is a JavaScript syntax extension that allows developers to write HTML-like syntax inside JavaScript to describe React elements.
It is compiled into JavaScript, typically React.createElement() calls, before being executed by the browser.
### JSX attributes
JSX attributes are properties specified on JSX elements to pass values, configure their behavior, or provide data to React components.
### JSX elements
JSX elements are HTML-like expressions written in JSX that describe React elements to be rendered by React.

Whenever you write something like:
```javascript
<h1>Hello World</h1>

or

<div>
    <p>Welcome</p>
</div>
```
or
```javascript
<Welcome name="Sajid" />
```
these are all JSX elements.

Types of JSX Elements
1. HTML JSX Elements
```javascript
<div>
    <h1>Hello</h1>
</div>
```
These represent HTML elements.

2. React Component JSX Elements
```javascript
<Welcome />

<Header />

<App />
```
These represent React components.

### What happens internally?

When you write:
```javascript
<h1>Hello</h1>

React (through Babel) conceptually converts it into:

React.createElement(
    "h1",
    null,
    "Hello"
);
```
Similarly,
```javascript
<Welcome name="Sajid" />

becomes conceptually:

React.createElement(Welcome, {
    name: "Sajid"
});
```
So JSX elements are just a syntax for creating React elements.
### Why JSX?
- Why use JSX?
- Easier to read
- Easier to write
- Looks similar to HTML
- Allows JavaScript inside markup
- Makes UI development simpler

### JSX Element vs React Component


```Javascript
React Component
function Welcome() {
    return <h1>Hello</h1>;
}
```
Welcome is a React component.

JSX Element
```javascript
<Welcome />
```
This is a JSX element.

React sees <Welcome /> and calls the Welcome component.

Visual Representation
```text
JSX Elements
│
├── HTML Elements
│      ├── <div>
│      ├── <button>
│      └── <input>
│
└── React Component Elements
       ├── <App />
       ├── <Header />
       └── <Welcome />
```
