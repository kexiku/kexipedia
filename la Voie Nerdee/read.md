The `read` command is a [[Bash]] builtin utility that reads a single line of text from [[Standard streams|standard input]].

It splits the line into words based on the [[IFS]] variable and assigns those words to one or more variables.

## 📜 Syntax

```bash
read [options] [names...]
```

## 📖 Common options

#### `-r`

- Disable backslash escaping

#### `-p`

- Display a prompt string before waiting for input

#### `-s`

- Silent mode
- Turns off character echoing
- Perfect for hiding sensitive data (passwords, tokens, etc.)





[^1]: Sources:
		https://linuxize.com/post/bash-read/
