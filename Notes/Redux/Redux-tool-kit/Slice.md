### Slice 

**Definition:**

A slice is a collection of related Redux logic, including a portion of the state, reducers, and automatically generated action creators.
  Example:
```javascript
const cartSlice = createSlice({
    name: "cart",
    initialState: [],
    reducers: {
        addItem() {},
        removeItem() {}
    }
});
```
Everything related to the cart lives in one place.
