A *command substitution* in [[Bash]] is a mechanism that replaces a command with its [[Standard streams|standard output]].

## 📜 Syntax

```bash
$(command)
```

## Examples

- Assign a current directory path to a variable:

```bash
current_dir=$(pwd)
```

- Change the default [[Shell types|login shell]] to bash:

```bash
chsh -s $(which bash)
```