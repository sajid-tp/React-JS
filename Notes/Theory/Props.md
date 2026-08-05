### Props
Props (short for Properties) are read-only values passed from a parent component to a child component to provide data or configuration.

### Why does props act like an object?

Because it is an object.

React creates this object automatically.

Suppose you write:
```javascript
<Welcome
    name="Sajid"
    age={22}
/>
```
React internally creates something conceptually like:
```javascript
const props = {
    name: "Sajid",
    age: 22
};
```
Then it calls your component:
``` javascript
Welcome(props);
```

which is equivalent to:
```javascript
Welcome({
    name: "Sajid",
    age: 22
});
```

### Flow
Parent Component
```text
<Welcome
    name="Sajid"
    age={22}
/>

          │
          ▼

React creates

{
    name: "Sajid",
    age: 22
}

          │
          ▼

Calls

Welcome(props)

          │
          ▼

Child Component

props.name
props.age
```

### Destructuring Props

Instead of:

function Welcome(props) {
    return <h1>{props.name}</h1>;
}

you can write:

function Welcome({ name, age }) {
    return (
        <>
            <h1>{name}</h1>
            <p>{age}</p>
        </>
    );
}

React still passes the same object.

JavaScript simply extracts the properties.
