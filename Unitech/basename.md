A `basename` command in [[Linux]] extracts the file name from a full path.

## ✂️ Usage

```bash
basename /etc/file.txt # Returns 'file.txt'
```

You can strip a file extension by providing it as the second argument:

```bash
basename /var/file.log .log # Returns 'file'
```
