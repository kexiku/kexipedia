## ✍️ Declaration
```jsx
let arr = [];
let arr = new Array();
let arr = Array.of();
```

## 📤 Getting elements

To get the last element of the array, instead of calculating the last element index we can use `.at()` method:
```jsx
const fruits = ["Apple", "Orange", "Plum"];

console.log( fruits.at(-1) ); // Plum
// same as fruits[fruits.length - 1]
```

## 🃏 Queue VS Stack

A _queue_ is an ordered collection of elements which supports two operations:

- `push` appends an element to the end.
- `shift` get an element from the beginning, advancing the queue, so that the 2nd element becomes the 1st.

![[CqutZ.png]]
*First in first out (FIFO)*

A _stack_ also supports two operations:

- `push` adds an element to the end.
- `pop` takes an element from the end.

A stack is usually illustrated as a pack of cards: new cards are added to the top or taken from the top:
![[fUtR1.png]]
*Last in first out (LIFO)*

Arrays in JavaScript can work both as a queue and as a stack. They allow you to add/remove elements, both to/from the beginning or the end.

> It’s much faster to work with the end of the array then the beginning 🏁

## 🔧 Methods

| _Icon_ | _Syntax_                                | _Description_                                                                                         | _Return value_                        | _Mutable_ |
| ------ | --------------------------------------- | ----------------------------------------------------------------------------------------------------- | ------------------------------------- | --------- |
| 👇     | `.push(element)`                        | adds elements to the _end_ of an array                                                                | array length                          | **M**     |
| 🫧     | `.pop()`                                | removes the _last_ element from an array                                                              | removed element                       | **M**     |
| 📥     | `.unshift(element)`                     | adds elements to the _beginning_ of an array                                                          | array length                          | **M**     |
| 📤     | `.shift()`                              | removes the _first_ element from an array                                                             | removed element                       | **M**     |
| 🍰     | `.slice(start, end)`                    | create a shallow copy of a portion of an array into a new array object selected from `start` to `end` | new array                             | **I**     |
| 🇨🇭   | `.splice(start, deleteCount, elements)` | removes the `deleteCount` elements staring from index `start` and insert `elements` in their place    | array containing the deleted elements | **M**     |
