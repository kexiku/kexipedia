## 🦄 Special characters

| _**Character**_  | _**Description**_                                                                                                                                                                                  |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `\t`             | Tab                                                                                                                                                                                                |
| `\n`             | New line                                                                                                                                                                                           |
| `\'`, `\"`       | Quotes                                                                                                                                                                                             |
| `\\`             | Backslash                                                                                                                                                                                          |
| `\r`             | In Windows text files a combination of two characters \r\n represents a new break, while on non-Windows OS it’s just \n. That’s for historical reasons, most Windows software also understands \n. |
| `\b`, `\f`, `\v` | Backspace, Form Feed, Vertical Tab – mentioned for completeness, coming from old times, not used nowadays (you can forget them right now).                                                         |

## 🔑 Accessing characters

To get a character at position `pos`, use square brackets or method `str.at(pos)`:
```jsx
let str = 'Coffee';

// the first character
console.log( str[0] ); // C
console.log( str.at(0) ); // C

// the last character
console.log( str[str.length - 1] ); // e
console.log( str.at(-1) ); // e
```
As you can see, the `.at(pos)` method has a benefit of allowing negative position _(If `pos` is negative, then it’s counted from the end of the string)._

We can also iterate over characters using `for..of`:
```jsx
for (let char of "Coffee") {
  console.log(char); // C,o,f,f,e,e
}
```

> ⚠️ **Strings are immutable** ⚠️

Strings can’t be changed in JavaScript. It is impossible to change a character.

## 🐫 Case

Methods [toLowerCase()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toLowerCase) and [toUpperCase()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toUpperCase) change the case:
```jsx
console.log( 'Sparta'.toUpperCase() ); // SPARTA
console.log( 'Sparta'.toLowerCase() ); // sparta
```

## 🔎 **Searching for a substring**

The first method is `str.indexOf(substr, pos)`

It looks for the `substr` in `str`, starting from the given position `pos`, and returns the position where the match was found (or `-1` if nothing was found):
```jsx
let str = 'Banana';

console.log( str.indexOf('na') ); // 2
console.log( str.indexOf('na', 3) ) // 4

console.log( str.indexOf('NA') ); // -1, not found, the search is case-sensitive
```

There is also a similar method [str.lastIndexOf(substr, position)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/lastIndexOf) that searches from the end of a string to its beginning.
it would list the occurrences in the reverse order.

The more modern method `str.includes(substr, pos)` returns `true/false` depending on whether `str` contains `substr` within:
```jsx
console.log( 'passion'.includes('ass') ) // true
```

The methods `str.startsWith()` and `str.endsWith()` do exactly what they say:
```jsx
console.log( 'funeral'.startsWith('fun') ) // true
console.log( 'nosegay'.endsWith('straight') ) // false
```

## 📬 Getting a substring

**`str.slice(start [, end])`**
Returns the part of the string from `start` to `end`:
```jsx
let str = "pineapple";
console.log( str.slice(0, 4) ); // pine
console.log( str.slice(4) ); // apple

console.log( str.slice(-5, -2) ); // app
// Negative values for start/end are also possible
```

`str.substring(start [, end])`
Almost the same as `slice`, but it allows `start` to be greater than `end` (in this case it simply swaps `start` and `end` values):
```jsx
let str = "pineapple";
console.log( str.substring(0, 4) ); // pine
console.log( str.substring(4, 0) ); // pine
```
Negative arguments are **not** supported.

`str.substr(start [, length])`
Returns the part of the string from `start`, with the given `length`:
```jsx
let str = "pineapple";
console.log( str.substr(0, 4) ); // pine
console.log( str.substr(4, 5) ); // apple

console.log( str.substr(-5, 3) ); // app
// The first argument may be negative, to count from the end
```

Let’s recap these methods to avoid any confusion:

| _Method_                | _Selects…_                                | _Negates_              |
| ----------------------- | ----------------------------------------- | ---------------------- |
| `slice(start, end)`     | from start to end (not including end)     | allows negatives       |
| `substring(start, end)` | between start and end (not including end) | negative values mean 0 |
| `substr(start, length)` | from start get length characters          | allows negative start  |





[^1]: Sources:
	<https://javascript.info/string>


