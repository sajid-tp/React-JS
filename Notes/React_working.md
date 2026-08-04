### Re-rendering conditions
- Its own state changes
  
```function Counter() {  
  const [count, setCount] = useState(0);  
  return (  
    <button onClick={() => setCount(count + 1)}>  
      {count}  
      </button>  
  );  
}```  
  
Clicking the button changes count.
Counter re-renders.
