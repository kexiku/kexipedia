## 🗺️ Map

[Map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map) is a collection of keyed data items which allows keys of any type.

Methods and properties:

- [`new Map()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map/Map) – creates the map.
- [`map.set(key, value)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map/set) – stores the value by the key.
- [`map.get(key)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map/get) – returns the value by the key.
- [`map.has(key)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map/has) – returns `true` if the `key` exists, `false` otherwise.
- [`map.delete(key)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map/delete) – removes the element (the key/value pair) by the key.
- [`map.clear()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map/clear) – removes everything from the map.
- [`map.size`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map/size) – returns the current element count.
- [`map.keys()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map/keys) – returns an iterable for keys,
- [`map.values()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map/values) – returns an iterable for values,
- [`map.entries()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map/entries) – returns an iterable for entries `[key, value]`, it’s used by default in `for..of`.


Every map.set call returns the map itself, so we can “chain” the calls:
```jsx
map.set('1', 'str1')
  .set(1, 'num1')
  .set(true, 'bool1');
```

## 🍱 Set

A [`Set`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set) is a special type collection where each value may occur only once.

Methods and properties:

- [`new Set(iterable)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set/Set) – creates the set, and if an `iterable` object is provided (usually an array), copies values from it into the set.
- [`set.add(value)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set/add) – adds a value, returns the set itself.
- [`set.delete(value)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set/delete) – removes the value
- [`set.has(value)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set/has) – returns `true` if the value exists in the set, otherwise `false`
- [`set.clear()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set/clear) – removes everything from the set.
- [`set.size`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set/size) – is the elements count.
- [`set.keys()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set/keys) – returns an iterable for values,
- [`set.values()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set/values) – same as `set.keys()`, for compatibility with `Map.`