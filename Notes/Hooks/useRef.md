### useRef()

Definition: A React Hook that returns a mutable ref object with a .current property, which persists across re-renders without causing a re-render when it changes. It's commonly used to directly access/reference a DOM element, or to store a mutable value that shouldn't trigger a UI update.

Syntax:

jsx
```javascript
const ref = useRef(initialValue);
```
Example (DOM access):

jsx
```javascript
function TextInput() {
  const inputRef = useRef(null);

  const focusInput = () => {
    inputRef.current.focus();
  };

  return (
    <>
      <input ref={inputRef} type="text" />
      <button onClick={focusInput}>Focus Input</button>
    </>
  );
}
```
Example (mutable value without re-render):

jsx
```javascript
function RenderCounter() {
  const renderCount = useRef(0);
  renderCount.current += 1;

  return <p>This component rendered {renderCount.current} times</p>;
}
```
