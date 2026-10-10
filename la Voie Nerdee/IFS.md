In Unix-like operation systems, *IFS* (stands for *Internal Field Separator*) is a special shell environment variable used by command-line interpreters to determine how strings are split into individual words during text processing.

By default, the shell sets `IFS` to include three whitespaces:

- Space (`' '`)
- Tab (`\t`)
- Newline (`\n`)

You can change the `IFS` value if you need to parse strings with non-standard delimiters, such as comma (`,`) or dash (`-`):

```bash
IFS=","
```

> [!tip]
> To avoid breaking subsequent commands that rely on whitespace separation, it is standard practice to save the original `IFS` value before changing it globally:
> ```bash
> # Save old IFS
> OLD_IFS=$IFS
> # Set custom IFS
> IFS=":"
> # ... run your code ...
> # Restore default IFS
> IFS=$OLD_IFS
> ```