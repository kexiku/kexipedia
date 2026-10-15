`zparseopts` is a built-in [[Zsh]] utility that extracts command flags and options directly into shell arrays

## 📜 Syntax

```zsh
zparseopts [ -D -E -F -K -M ] [ -a array ] [ -A assoc ] -- SPECS
```

### `-D`

- Delete matched options from the positional parameters (`$@`)

### `-E`

- Allows flags and positional arguments to be mixed

### `-F`

- Exit immediately if an invalid flag is encountered

### `-a array`

- Store options into a standard indexed array

### `-A assoc`

- Store options into an associative array
