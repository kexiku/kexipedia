The `printf` command in [[Bash]] is a powerful shell builtin used to format and print text.

It serves as a more reliable and feature-rich replacement for `echo`, mirroring the behavior of the C language's `printf()` function.

## 📜 Syntax

```bash
printf [-v var] "FORMAT" [arguments...]
```

#### `-v`

- tells `printf` not to print the output but to assign it to the variable (`var`)

#### FORMAT

- A string that may contain three different types of objects:
	- Regular characters (printed to output as-is)
	- Backslash-escaped special characters (like `\n` for new line)
	- Format specifiers

#### arguments

- Values that replace specifiers in the format string

## Common format specifiers

| Specifier    | Description                              | Example                 |
| ------------ | ---------------------------------------- | ----------------------- |
| `%s`         | Formats the argument as a literal string | `printf "%s\n" "Hello"` |
| `%d` or `%i` | Formats a signed decimal integer         | `printf "%d" 42`        |
| `%f`         | Formats a floating-point number          | `printf "%f" 3.14`      |
| `%%`         | Prints a literal percent sign (`%`)      | `printf "100%%"`        |

## Key Differences from `echo`

- No Automatic Newline
- Format Reusability
- Consistency





[^1]: Sources:
		https://linuxize.com/post/bash-printf-command/
