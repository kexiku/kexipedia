[[Zsh]] *path modifiers* like `:h`, `:t`, and `:r` let you slice up file paths directly without calling external tools like `dirname` or `basename`.

## 📂 Core path modifiers

### `:h` (head)
- Keeps the directory path and drops the final component
- Example: `${/path/to/file:h}` → `/path/to`

### `t` (tail)
- Keeps only the last path component
- Example: `${/path/to/file:t}`→ `file`

### `:r` (root)
- Removes the file extension from the filename
- Example: `${/some/file.txt:r}` `/some/file`

You can also chain the modifiers from left to right to apply them consistently.