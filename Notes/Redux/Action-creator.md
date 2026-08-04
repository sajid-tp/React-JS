### Action

**Definition:**

An action is a plain JavaScript object that describes what happened in the application.

An action does not update the state.

It only describes an event.


```javascirpt
{
  type: "cart/addItem",
  payload: product
}
```

### Action Creator 


**Definition:**
An action creator is a function that creates and returns an action object.

Instead of writing actions manually,
```javascript
{
  type: "cart/addItem",
  payload: product
}
```
you write,
```javascript
const addItem = (product) => {
  return {
    type: "cart/addItem",
    payload: product
  };
};
```
