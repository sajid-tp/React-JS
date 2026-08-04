### Reducer
- A reducer is a pure function that receives the current state and an action, and returns the next state.
- Its only responsibility is deciding how the state should change.

Example:
```javascript
(state, action) => {
    state.cart.push(action.payload);
}
```
The reducer answers:

Given the current state and this action, what should the new state be?
