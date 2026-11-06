A double dash (`--`) is used in [[Bash]] scripts to signify the end of command options.

Once the command encounters `--`, it stops looking for internal flags starting with a hyphen `-`.
Everything following the double dash is treated as a positional parameter, file name, or operand.

It's especially useful for handling files whose names starts with `-`, which would otherwise be treated as a command options:

```bash
rm -- -rf # Safely deletes the file named '-rf'
```

Another use case is grepping patterns starting with a dash:

```bash
grep -- "--help" file.txt
```
