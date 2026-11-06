- Add files to the index:

```bash
git add <file_path>
```

![[Screenshot 2024-08-13 195911.webp]]

- Create a commit:

```bash
git commit -m "<message>"
```

- modify the most recent commit:

```bash
git commit --amend
```

- See the exact date the file was added to repo:

```bash
git log --diff-filter=A --follow --format=%ad --date=short -- README.md
```

- `--diff-filter=A` → show commits where the file was added
- `--follow` → follow the file across renames
- `--format=%ad` and `--date=short`→ format the output to display just the date
- `-- path/to/file` → only inspect that file





---

<small>Sources:</small>
<small>• https://git-scm.com</small>