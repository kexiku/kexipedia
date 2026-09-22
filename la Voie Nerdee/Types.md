## String Concatenation

- If the binary `+` is applied to strings, it merges (concatenates) them
- If any of the operands is a string, then the other one is converted to a string too
```jsx
console.log('pine' + 'apple'); // pineapple
console.log('1' + 2 + 3); // 123
console.log(1 + 2 + '3'); // 33
```

## Boolean Conversion

- Intuitively “empty” values like `0`, an empty string, `null`, `undefined`, and `NaN`, become `false`
- Other values become `true`

## 🔢 Number Conversion

| _Value_                                              | _Becomes…_                                                                     |
| ---------------------------------------------------- | ------------------------------------------------------------------------------ |
| `undefined`                                          | `NaN`                                                                          |
| `null`                                               | `0`                                                                            |
| `true` and `false`                                   | `1` and `0`                                                                    |
| string                                               | Whitespaces (includes tabs, newlines etc.) from the start and end are removed. |
| If the remaining string is empty, the result is `0`. |                                                                                |
| Otherwise, the number is “read” from the string.     |                                                                                |
| An error gives `NaN`.                                |                                                                                |





[^1]: Sources:
	[https://javascript.info/type-conversions](https://javascript.info/type-conversions)
	[https://javascript.info/operators](https://javascript.info/operators)
