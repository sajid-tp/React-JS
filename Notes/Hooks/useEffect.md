### useEffect()

- A React Hook that lets you perform side effects in function components — such as fetching data, subscribing to events, manually changing the DOM, or setting timers. 
- It runs after the component renders, and can optionally re-run when specified dependencies change. 
- It can also return a cleanup function that runs before the component unmounts or before the effect re-runs.

Syntax:

jsx
```javascript
useEffect(() => {
  // side effect code
  return () => {
    // optional cleanup code
  };
}, [dependencies]);
```
Behavior based on the dependency array:


| Dependency Array | When it runs |
|------------------|--------------|
| Omitted | After every render |
| `[]` (empty) | Only once, after the initial render |
| `[a, b]` | After the initial render, and whenever `a` or `b` changes |


Example:
```javascript
jsx
function Timer() {
  const [seconds, setSeconds] = useState(0);

  useEffect(() => {
    const interval = setInterval(() => setSeconds(s => s + 1), 1000);
    return () => clearInterval(interval); // cleanup
  }, []);

  return <p>{seconds}s elapsed</p>;
}
```
