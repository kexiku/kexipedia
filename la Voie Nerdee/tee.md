---
banner: tee.webp
banner_icon: ☕
banner_y: 90.4%
---
*Tee* command writes the standard input to both standard output *and* one or more files.

By default, it replaces the content of the target file; to preserve the file content, use `-a` flag:

```bash
<program> | tee -a output.txt
```