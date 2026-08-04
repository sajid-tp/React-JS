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

How it works

When you dispatch:
```javascript
dispatch(fetchProducts());
```
Redux Toolkit does this internally:
```text
dispatch(fetchProducts.pending)

↓

Run async function

↓

Success?

↓

dispatch(fetchProducts.fulfilled)
```
or
```javascript
dispatch(fetchProducts.rejected)
```
You don't dispatch those three actions yourself.

Example
```javascript
export const fetchUsers = createAsyncThunk(
  "users/fetchUsers",
  async () => {
    const response = await fetch("/users");
    return response.json();
  }
);
```
In your slice:
```javascript
const usersSlice = createSlice({
  name: "users",
  initialState: {
    users: [],
    loading: false,
    error: null,
  },
  reducers: {},
  extraReducers: (builder) => {
    builder
      .addCase(fetchUsers.pending, (state) => {
        state.loading = true;
      })
      .addCase(fetchUsers.fulfilled, (state, action) => {
        state.loading = false;
        state.users = action.payload;
      })
      .addCase(fetchUsers.rejected, (state, action) => {
        state.loading = false;
        state.error = action.error.message;
      });
  },
});
```
What does it generate?

Suppose you write:
```javascript
createAsyncThunk(
    "users/fetchUsers",
    async () => { ... }
);
```
Redux Toolkit automatically creates these action types:
```text
users/fetchUsers/pending

users/fetchUsers/fulfilled

users/fetchUsers/rejected
```
