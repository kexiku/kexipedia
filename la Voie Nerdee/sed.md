*sed* (short for *stream editor*) is a line-by-line text processing utility.

It's commonly used in shell scripts to perform basic text transformations on an input stream, such as file or pipeline.

## 📜 Syntax
```bash
sed [OPTIONS] 'COMMAND' [INPUTFILE...]
```

## 🪶 Usage

- Edit the file in-place (overwrite):
```bash
sed -i 's/foo/bar/' file.txt
```

- Replace the text:
```bash
sed 's/OLD/NEW/' file.txt
# OR
sed 's|OLD|NEW|' file.txt
```