## ✍️ Syntax
```jsx
let promise = new Promise(function(resolve, reject) {
  // executor (the producing code, "singer")
});
```
The promise object returned by the `new Promise` constructor has these internal properties:

- `state` — initially "pending", then changes to either "fulfilled" when `resolve` is called or "rejected" when `reject` is called.
- `result` — initially `undefined`, then changes to `value` when `resolve(value)` is called or `error` when `reject(error)` is called.
![[Screenshot 2024-10-04 141124.webp]]

## 🍔 Consumers

### 🥏 **then**
```jsx
promise.then(
  function(result) { /* handle a successful result */ },
  function(error) { /* handle an error */ }
);
```

### 🏓 **catch**
```jsx
promise.catch(
  function(error) { /* handle an error */ }
);
```
The call `.catch(f)` is a complete analog of `.then(null, f)`, it’s just a shorthand.

### 🏁 **finally**
```jsx
promise.finally(
  function() { /* runs always, when the promise is resolve or reject */ }
);
```
A `finally` handler “passes through” the result or error to the next suitable handler.

For instance, here the result is passed through `finally` to `then`:
```jsx
new Promise((resolve) => {
	setTimeout(() => resolve("value"), 1000);
})

.finally(() => alert("Promise ready")) // triggers first
.then(result => alert(result)); // <-- shows "value"
```





[^1]: Sources:
	[https://javascript.info/promise-basics](https://javascript.info/promise-basics)
	[https://javascript.info/promise-chaining](https://javascript.info/promise-chaining)
