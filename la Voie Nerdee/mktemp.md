Create a temporary file or directory.

## 📜 Syntax

```bash
mktemp [OPTIONS...] [TEMPLATE]
```

Template should be in format `filename.XXX`, when `X` characters are placeholders that `mktemp` replaces with random characters.

> [!note]
> At least 3 consecutive `X`'s are required at the end of the template string

## Common options

### `-d`

- Create a temporary directory