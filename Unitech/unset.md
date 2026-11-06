The `unset` command is a built-in [[Bash]] utility used to remove variables and functions from the [[shell]]'s memory.

It completely undefines the target name, dropping both its value and its associated attributes.

> [!warning]
> If `set -u` option is enabled in a Bash script, the shell exits immediately with an error whenever an unset variable is referenced.

## Usage

- Unset a variable:

```bash
unset var
```

- Unset a function:

```bash
func () { ... }
unset -f func
```

