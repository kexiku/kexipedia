Sometimes you don't want specific files to be tracked by [[Git]] - in this case, you can tell Git to *ignore* them.

This is useful for keeping logs, build artifacts, private keys or any other files out of your repository.

Ignored files are listed in a special file named `.gitignore` that should be placed at the root of your repository.

The `.gitignore` file itself is tracked by Git, so everyone using the repository ignores the same files.

## 📝 Patterns

| Pattern          | Matches                                                       | Explanation                                                                                    |
| ---------------- | ------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `logs`           | `/build/logs`<br>`/logs/debug.log`                            | Matches both files and directories                                                             |
| `logs/`          | `/logs/debug.log`                                             | Appending a slash indicates the pattern is a directory                                         |
| `*.log`          | `/.log`<br>`/debug.log`<br>`/logs/debug.log`                  | Matches any number of characters                                                               |
| `*.ext`          | `/log.ext`<br>`/build/log.ext`                                | Matches all files with `.ext` extention                                                        |
| `**/logs`        | `/build/logs/debug.log`                                       | Matches files anywhere in the repo                                                             |
| `/debug.log`     | `/debug.log`<br>*but not*<br>`/logs/debug.log`                | Matches files only in the repo's root<br>*(by default, patterns match files in any directory)* |
| `debug?.log`     | `/debugX.log`<br>*but not*<br>`/debug10.log`                  | Matches exactly one character                                                                  |
| `debug[0-9].log` | `/debug0.log`<br>`/debug1.log`<br>*but not*<br>`/debug10.log` | Matches a single character in the specified range<br>*(numeric or alphabetic)*                 |
| `debug[01].log`  | `/debug0.log`<br>`/debug1.log`<br>*but not*<br>`/debug2.log`  | Matches a single character in the specified set<br>*(numeric or alphabetic)*                   |
You can use `#` for comments:

```bash
# ignore all logs
*.log
```

To exclude a pattern from being ignored, use the `!` operator:

```bash
# Ignore all .log files except important.log
*.log
!important.log
```

> [!warning]
> You cannot exclude a file if its ignored pattern matching a directory.
> 
> Thus, the following rules will not work:
> ```bash
> logs/ 
> !logs/important.log
> ```

To ignore a file that have already been committed, you need to untrack it first:

```bash
git rm --cached debug.log
```

The `--cached` option only removes a file from the index, keeping it in your working directory; omit it if you want to delete the file from both the index and your local file system.





---

<small>Sources:</small>
<small>• https://www.w3schools.com/git/git_ignore.asp?remote=github</small>
<small>• https://gist.github.com/jstnlvns/ebaa046fae16543cc9efc7f24bcd0e31</small>
