The `export` is a [[Bash]] builtin used to pass local variables to child [[processes]], making them available as [[environment variables]].

 Variables that haven't been exported are only available in the current [[shell]] session and aren't inherited by child processes.

## 🚛 Usage

- Export a variable:

```bash
export VAR="value"
```

- Export a function:

```bash
func() { ... }
export -f func
```

> [!warning]
> Unlike variables, Bash function syntax doesn't allow the `export` keyword to be added before the function definition: a function must be declared first, and only then can be exported

## ⛓️‍💥 Unsetting

Exported variables usually don't need to be explicitly [[unset]] when a script is executed normally, since they disappear when the script's process terminates.

However, when a script is [[Source|sourced]], its variables become a part of the calling shell's environment and may persist after execution.
In this case, consider using `unset` to remove temporary variables.
