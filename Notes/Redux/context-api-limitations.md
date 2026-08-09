### Limitations of Context API

- Re-renders everything – Any change to context value re-renders all consuming components, even ones that don't use the changed part.
- No state management logic – Context only passes data; you still need useState/useReducer to actually manage how state updates.
- No middleware – No built-in way to handle async logic (API calls, logging, etc.) — you have to hand-roll it with useEffect.
- No dev tools – No time-travel debugging or action history like Redux DevTools gives you.
- Not built for frequent updates – Works fine for rarely-changing data (theme, auth), but performs poorly with fast/complex state changes (forms, real-time data).

---
- No structure → unpredictable updates  
- No selectors → unnecessary re-renders  
- No middleware/devtools → no way to trace why something re-rendered or changed  
