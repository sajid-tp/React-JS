### Middleware
Middleware is a function that sits between dispatch() and the reducer, allowing you to intercept, modify, delay, or perform additional work before an action reaches the reducer.

**Visual Flow**

```text
dispatch(action)
       │
       ▼
Middleware
       │
       ▼
Reducer
       │
       ▼
Updated State
```

### Why middleware?

- Primary use 1: Handle asynchronous operations

Imagine you want to fetch products from a server.

Without middleware:

dispatch(fetchProducts());

A reducer cannot do this:

// Wrong
```javascript
const reducer = (state, action) => {
    const data = await fetch("/products");
}
```
Reducers must be synchronous.

Instead, thunk middleware does:
```text
dispatch(fetchProducts())
        │
        ▼
Thunk Middleware
        │
        ├── Make API request
        ├── Wait for response
        └── Dispatch success action
                │
                ▼
Reducer
```

- Primary use 2: Logging

Every action can be logged.
```text
dispatch(addItem())

↓

Logger Middleware

↓

Action: cart/addItem

↓

Reducer
```

Useful while debugging.

- Primary use 3: Validation

Before allowing an action to continue:
```text
dispatch(deleteAccount())

↓

Middleware

↓

Is user authenticated?

↓

Yes → Continue

No → Stop
```
- Primary use 4: Analytics

Example:
```text
User clicks Buy

↓

Middleware

↓

Send analytics event

↓

Reducer
```
