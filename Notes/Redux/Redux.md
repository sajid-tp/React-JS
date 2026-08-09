### What is redux?
- Redux is a JavaScript library for managing and centralizing an application's state in a predictable way.
- It stores the application's shared state in a single store and updates that state predictably through actions and reducers.

### Why Redux

- Better for complex state management  
Redux provides a structured way to manage large amounts of shared state.
- Predictable state updates  
State changes happen through actions → reducers, making it easier to understand how and why state changed.
- Powerful debugging with Redux DevTools  
You can see actions, previous state, next state, and track exactly what changed.
- Better handling of frequent state updates  
Redux's selector-based approach can help components subscribe only to the state they need, avoiding some unnecessary re-renders that can happen with Context.
- Excellent ecosystem and middleware support  
Redux works well with middleware and Redux Toolkit features such as createAsyncThunk, making API calls and other side effects easier to organize.
In one sentence:

Context is mainly for sharing data; Redux is for managing complex shared application state in a predictable, debuggable, and structured way.
