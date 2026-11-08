The `source` command in [[Bash]] is a [[shell]] builtin used to read and execute commands from a [[scripts|script]] file within the current shell session.

When a script is run using `source`, any variables created or modified by the script will remain available after the script completes.

It is generally used in Bash scripts to define functions or variables that should be available across all the script parts.

Another common use case for `source` is reloading the shell config without opening a new terminal window:

```bash
source ~/.bashrc # For example
```

Unlike other [[Scripts execution|script execution]] methods, sourcing doesn't require a [[shebang]] or executable [[permissions]], as it runs scripts in the current shell session rather than spawning a new subshell (i.e. no new [[processes]] are launched).

## 📒 Usage

```bash
source filename [...SCRIPT_FILES]
# OR
. filename [...SCRIPT_FILES]
```

The dot-notation syntax is [[POSIX]]-compliant and is recommended to use in cases where compatibility is a priority.





---

<small>Sources:</small>
<small>• https://ss64.com/bash/source.html</small>
<small>• https://linuxize.com/post/bash-source-command/</small>
