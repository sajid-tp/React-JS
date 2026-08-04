### createAsyncThunk
createAsyncThunk is a Redux Toolkit utility that simplifies writing asynchronous logic (such as API calls) by automatically generating and dispatching pending, fulfilled, and rejected actions.

### Why do we need createAsyncThunk?

Imagine you want to fetch products.

Without createAsyncThunk, you'd have to write:
```text
dispatch(fetchStarted())

↓

API Call

↓

Success?
   │
   ├── Yes → dispatch(fetchSucceeded())
   │
   └── No → dispatch(fetchFailed())
```
You write all of this manually.

With createAsyncThunk:
```javascript
export const fetchProducts = createAsyncThunk(
    "products/fetchProducts",
    async () => {
        const response = await fetch("/products");
        return response.json();
    }
);
```
That's it.

Redux Toolkit automatically dispatches:
```text
products/fetchProducts/pending

↓

products/fetchProducts/fulfilled

or

products/fetchProducts/rejected
```
