### useNavigate()
Definition
useNavigate() is a React Router Hook that returns a function used to programmatically navigate between routes in a React application.

Example
```javascript
import { useNavigate } from "react-router-dom";

function Login() {
    const navigate = useNavigate();

    const handleLogin = () => {
        navigate("/dashboard");
    };

    return <button onClick={handleLogin}>Login</button>;
}
```
Here:

useNavigate() returns the navigate function.
Calling navigate("/dashboard") changes the route to /dashboard.
