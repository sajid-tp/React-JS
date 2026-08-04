### configureStore()

**Definition:**
configureStore() is a Redux Toolkit function that sets up and creates the Redux store, automatically combining your reducers, adding the Redux Thunk middleware, enabling Redux DevTools, and applying good default configurations

```javascript
import { configureStore } from '@reduxjs/toolkit';

const store = configureStore({
  reducer: {
    cake: cakeSlice.reducer,
    iceCream: iceCreamSlice.reducer
  }
});
```
