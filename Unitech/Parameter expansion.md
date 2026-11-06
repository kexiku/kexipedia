[[Bash]] *parameter expansion* is the mechanism the [[shell]] uses to substitute a variable or parameter with its actual value.

Beyond simple evaluation (like `$var` or `${var}`), the `${...}` syntax unlocks a powerful built-in toolkit for string manipulation, pattern matching and case modification.

Using the native parameter expansion is significantly faster than piping to external commands like `sed` because it runs inside the current Bash [[Processes|process]] without spawning a subprocess.

## 💲 Common operations

- Evaluate to `default` if `$var` is unset or empty:

```bash
${var:−default}
```

- Evaluate to `default` and *assign* it to `$var` if it's unset or empty:

```bash
${var:=default}
```

- Exits script with `error_msg` if `$var` is unset or empty:

```bash
${var:?error_msg}
```

- Returns the number of characters in the string:

```bash
${#var}
```

- Deletes the *shortest* match of a `pattern` from the *left* side:

```bash
${var#pattern}
```

- Deletes the *longest* match of a `pattern` from the *left* side:

```bash
${var##pattern}
```

- Deletes the *shortest* match of a `pattern` from the *right* side:

```bash
${var%pattern}
```

- Deletes the *longest* match of a `pattern` from the *right* side:

```bash
${var%%pattern}
```

- Replaces the first occurrence of `pattern` with `replacement`:

```bash
${var/pattern/replacement}
```

- Replaces *every* occurrence of `pattern` with `replacement`:

```bash
${var//pattern/replacement}
```

- Converts the entire string to uppercase/lowercase:

```bash
${var^^} # Uppercase
${var,,} # Lowercase
```

- Extract the directory portion from path (alternative to [[dirname]]):

```bash
${path%/*}
```

- Extract the file name from path (alternative to [[basename]]):

```bash
${path##*/}
```




---

<small>Sources:</small>
<small>• https://www.gnu.org/software/bash/manual/html_node/Shell-Parameter-Expansion.html</small>
