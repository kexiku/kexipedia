[[Bash]] *parameter expansion* is the mechanism the shell uses to substitute a variable or parameter with its actual value.

Beyond simple evaluation (like `$var` or `${var}`), the `${...}` syntax unlocks a powerful built-in toolkit for string manipulation, pattern matching and case modification.

Using the native parameter expansion is significantly faster than piping to external commands like `sed` because it runs inside the current Bash [[Processes|process]] without spawning a subprocess.

## 💲 Common operations

### `${var:−default}`

- Evaluate to `default` if `$var` is unset or empty

### `${var:=default}`

- Evaluate to `default` and *assign* it to `$var` if it's unset or empty

### `${var:?error_msg}`

- Exits script with `error_msg` if `$var` is unset or empty

### `${#var}`

- Returns the number of characters in the string

### `${var#pattern}`

- Deletes the *shortest* match of a `pattern` from the *left* side

### `${var##pattern}`

- Deletes the *longest* match of a `pattern` from the *left* side

### `${var%pattern}`

- Deletes the *shortest* match of a `pattern` from the *right* side

### `${var%%pattern}`

- Deletes the *longest* match of a `pattern` from the *right* side

### `${var/pattern/replacement}`

- Replaces the first occurrence of `pattern` with `replacement`

### `${var//pattern/replacement}`

- Replaces *every* occurrence of `pattern` with `replacement`

### `${var^^}` / `${var,,}`

- Converts the entire string to uppercase / lowercase





[^1]: Sources:
		https://www.gnu.org/software/bash/manual/html_node/Shell-Parameter-Expansion.html`
