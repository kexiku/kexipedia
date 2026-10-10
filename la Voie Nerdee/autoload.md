In [[Zsh]], `autoload` is a built-in command that tells the shell to load an external function only when that function is first called, rather than loading it immediately at shell startup.

This reduces the shell startup time because the shell doesn't parse hundreds of function code lines until you actually need them.

The concept of `autoload` command is also known as *"lazy loading"*.

## 🚩 Common flags

### `-U`
- Prevent any custom aliases from expanding inside the function code when it is being loaded (use native aliases instead)

### `-z`
- Force the function to load using native zsh style rather than KornShell (ksh) compatibility mode