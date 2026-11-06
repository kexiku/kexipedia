The `realpath` command in [[Linux]] converts each filename argument to an absolute pathname.

By default, it expands all [[symbolic links]] and resolves redundant path elements like `.` and `..`.

## 🛤️ Usage

```bash
realpath doc.pdf # → /home/user/Documents/doc.pdf
realpath ../Pictures/logo.png # → /home/user/Pictures/logo.png
realpath shortcut # → /home/user/.local/bin/shortcut
```





---

<small>Sources:</small>
<small>• https://man7.org/linux/man-pages/man3/realpath.3.html</small>
