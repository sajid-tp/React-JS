
### useState()

Definition: A React Hook that lets you add and manage local state in a function component. It returns an array with two elements: the current state value, and a function to update it. When the update function is called, React re-renders the component with the new value.

Syntax:

jsx
```javascript
const [state, setState] = useState(initialValue);
```
Example:

jsx
```javascript
function Counter() {
  const [count, setCount] = useState(0);

  return (
    <button onClick={() => setCount(count + 1)}>
      Count: {count}
    </button>
  );
}
```
