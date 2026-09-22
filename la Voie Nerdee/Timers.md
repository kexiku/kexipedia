## setTimeout
```jsx
let timerId = setTimeout(func, [delay], [func arguments]...);
```

## setInterval
```jsx
let timerId = setInterval(func, [delay], [func arguments]...);

// (same syntax)
```

> **Nested `setTimeout` allows to set the delay between the executions more precisely than `setInterval`** 🤌

- To cancel the execution, we should call `clearTimeout/clearInterval` with the value returned by `setTimeout/setInterval`