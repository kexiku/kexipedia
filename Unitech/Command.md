A [[Bash]] builtin used to locate a command.

It allows you to distinguish the actual command from aliases or [[functions]] with the same name.

## 📍 Usage

- Check if a command exists:

```bash
command -v <command> &>/dev/null # silence the output
```

> [!tip]
> In modern scripting, it's preferable to use `command -v` instead of `which`:
> - It's a shell builtin 
> - It complies with the [[POSIX]] standard





---

<small>Sources:</small>
<small>• https://stackoverflow.com/questions/37056192/which-vs-command-v-in-bash</small>
<small>• https://www.gnu.org/software/bash/manual/html_node/Bash-Builtins.html</small>
