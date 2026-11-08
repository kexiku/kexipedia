The `readonly` command is a [[Bash]] built-in utility used to make variables or functions immutable.

Once an item is marked as read-only, its value cannot be changed by subsequent assignments nor be [[unset]].

## 📖 Usage

- Define a read-only variable:

```bash
readonly VAR="constant_value"
```

- Mark an existing variable as read-only:
 
```bash
API_KEY="12345"
readonly API_KEY
```

- Mark an existing function as read-only:

```bash
readonly -f func
```

> [!warning]
> Bash syntax doesn't allow to define function as read-only during its definition: a function must be declared first, and only then can be marked as read-only





---

<small>Sources:</small>
<small>• https://www.geeksforgeeks.org/linux-unix/shell-scripting-readonly-command</small>
