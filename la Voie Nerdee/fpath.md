In [[Zsh]], `$fpath` (*function path*) is a special [[Environment variables|environment]] parameter that stores an array of directories where the shell searches for autoloaded function definitions and completion scripts.

It behaves similarly to the standard `$PATH` variable, but instead of searching for executable binaries, it searches for script files.

## 🔍 How it Works

When you ask zsh to load a function or a completion script using the `autoload` command, it doesn't load the function into memory immediately.
Instead, it searches the directories listed in `$fpath` for a file that matches the function name.
When the function is finally called, zsh reads and executes the contents of the function file.