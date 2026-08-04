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

### Payload

**Definition:**

The payload is the data carried by an action that provides the information needed to update the state.

Example:
```
dispatch(addItem(product));
```
The product is the payload.

Action:
```
{
    type: "cart/addItem",
    payload: product
}
```
