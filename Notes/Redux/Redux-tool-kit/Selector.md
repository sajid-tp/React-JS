### Selector

**Definition:**

A selector is a function used to read specific data from the Redux store.

Example:
```javascript
const cart = useSelector(state => state.cart);
```
Selectors only read state.

They never modify it.
