The [[Linux]] `readlink` command displays the path of a target file or directory that a [[symbolic links|symbolic link]] points to.

## 🔗 Usage

- Get the absolute path of a symlink target:

```bash
readlink -f <link>
```

This command follows all symlinks recursively to canonicalize the path.

> [!tip]
> Always use `-f` flag when calling `readlink` in scripts to avoid errors caused by providing relative path where the full path was expected
