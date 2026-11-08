The `export` is a [[Bash]] builtin used to pass local variables to child [[processes]], making them available as [[environment variables]].

 Variables that haven't been exported are only available in the current [[shell]] session and aren't inherited by child processes.

## 🚛 Usage

- Export a variable:

```bash
export VAR="value"
```

- Export an existing function:

```bash
func() { ... }
export -f func
```

> [!warning]
> Bash syntax doesn't allow the `export` keyword before the function definition: a function must be declared first, and only then can be exported

## ⛓️‍💥 Unsetting

Exported variables usually don't need to be explicitly [[unset]] in script files, since they disappear when the script's process terminates.

However, when a script is [[Source|sourced]] from an [[Shell types|interactive shell]], its variables become a part of the shell's environment and may persist after execution.
In this case, use `unset` command to remove them.
