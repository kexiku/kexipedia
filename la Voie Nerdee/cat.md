The `cat` (*concatenate*) command in [[Linux]] is a core utility used to view, create, and combine file contents directly from the terminal.

It allows users to perform simple operations with file content without opening a text editor.

> [!tip]
> To view a file content in reversed order, use the **`tac`** command

## 🐈 Usage

- View the content of a single file:
`
```bash
cat file_name
```

## 📝 Heredoc

The *heredoc* (short for "*here document*") is a handy way to pass multiline blocks of text directly into a command or a file without using multiple `echo` statements.

- Syntax:

```bash
cat <<EOF
... some text ...
EOF
```




[^1]: Source:
		https://www.geeksforgeeks.org/linux-unix/cat-command-in-linux-with-examples/
