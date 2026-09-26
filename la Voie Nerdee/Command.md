A shell builtin used to locate a command and check if it exists.

> [!tip]
> In modern scripting, it's preferable to use `command -v` instead of `which` since it complies with the [[POSIX]] standard and is a shell built-in while `which` is an external binary

## ❔ Usage

- Check if a command exists:
```bash
command -v <command>
```





[^1]: Sources:
	https://stackoverflow.com/questions/37056192/which-vs-command-v-in-bash
