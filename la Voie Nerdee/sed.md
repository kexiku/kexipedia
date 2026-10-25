*sed* (short for *stream editor*) is a line-by-line text processing utility in [[Linux]].

It's commonly used in shell scripts to perform basic text transformations on an input stream, such as [[Files|file]] or [[Pipelines|pipeline]], using [[regular expressions]].

## 📜 Syntax

```bash
sed [OPTIONS] 'COMMAND' [INPUTFILE...]
```

## ✂️ Usage

- Replace the text in file:

```bash
sed -i 's/OLD/NEW/' file.txt
# OR
sed -i 's|OLD|NEW|' file.txt
```

The `-i` flag stands for *in-place* editing: without it, `sed` would just print the modified text to the terminal output.