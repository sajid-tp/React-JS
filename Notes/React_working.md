### Re-rendering conditions
- Its own state changes
  
```javascript
function Counter() {  
  const [count, setCount] = useState(0);  
  return (  
    <button onClick={() => setCount(count + 1)}>  
      {count}  
      </button>  
  );  
} 
```
Clicking the button changes count.  
Counter re-renders.

- Its parent re-renders
```javascript
function App() {
  const [count, setCount] = useState(0);

  return <Child />;
}
```

When count changes,App re-renders.
By default, React also renders Child again.

App re-renders
      ↓
Child re-renders

Even if Child has no props. 
- The props it receives change ✅
```javascript
function App() {
  const [name, setName] = useState("Sajid");

  return <Child name={name} />;
}
```
If name changes,
Child receives a new prop.
Child re-renders.

- The context value changes 
```
<ThemeContext.Provider value={theme}>
```

Suppose

theme = "light"

becomes

theme = "dark"

Every component using
```
useContext(ThemeContext)
```
re-renders.
