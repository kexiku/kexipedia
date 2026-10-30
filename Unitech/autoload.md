In [[Zsh]], `autoload` is a built-in command that tells the shell to load an external function only when that function is first called, rather than loading it immediately at startup.

This reduces the shell startup time because the shell doesn't parse any autoloaded functions at the initialization stage.

The concept of `autoload` command is also known as *"lazy loading"*.

## 🔄 Options

### `-U`

- Prevent any custom aliases from expanding inside the function code when it's being loaded

### `-z`

- Force the shell to load function using native zsh style *(no KornShell compatibility mode)*

> [!tip]
> The most common usage of the `autoload` command is to initialize the [[Zsh completions|completion system]] for the current session:
> 
> ```zsh
> autoload -Uz compinit; compinit
> ```





[^1]: Sources:
		https://thevaluable.dev/zsh-completion-guide-examples/
