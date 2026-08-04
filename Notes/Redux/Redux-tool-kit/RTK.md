### Redux Toolkit

**Definition:**

Redux Toolkit is the official, recommended way to write Redux applications. It simplifies Redux by reducing boilerplate and providing built-in best practices.

It provides:

- configureStore()
- createSlice()
- createAsyncThunk()
- Immer integration
- DevTools support

| API | Purpose |
|------|---------|
| `configureStore` | Sets up the Redux store. Automatically includes `combineReducers`, Redux DevTools, and thunk middleware. |
| `createSlice` | Generates action types, action creators, and a reducer function from a single configuration object. |
| `createAsyncThunk` | Simplifies asynchronous logic (such as API calls) by automatically generating `pending`, `fulfilled`, and `rejected` actions. |
| `createReducer` | Lets you write reducers using mutating-style syntax (powered by Immer) instead of `switch` statements. |
| `createSelector` | Creates memoized selectors (using Reselect) to improve performance by avoiding unnecessary recalculations. |
