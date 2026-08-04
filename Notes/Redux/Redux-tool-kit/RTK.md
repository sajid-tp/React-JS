### Redux Toolkit

**Definition:**

Redux Toolkit is the official, recommended way to write Redux applications. It simplifies Redux by reducing boilerplate and providing built-in best practices.

It provides:

- configureStore()
- createSlice()
- createAsyncThunk()
- Immer integration
- DevTools support

|configureStore|	Sets up the store — auto-includes combineReducers, Redux DevTools, and thunk middleware|
|createSlice|	Generates action types, action creators, and a reducer function, all from one object|
createAsyncThunk	Simplifies dispatching async logic (like API calls) with automatic pending/fulfilled/rejected actions
createReducer	Lets you write reducers using a mutating-style syntax (via Immer) instead of switch statements
createSelector (via reselect)	Builds memoized selectors for performance
