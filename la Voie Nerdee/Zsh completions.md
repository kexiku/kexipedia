[[Zsh]] has two completion systems:

- The old *compctl*
- And the more recent *compsys*

When you type a command in Zsh and hit the `TAB` key, a completion is attempted depending on the *context*.

The context includes:

- What command have been already typed at the prompt
- Where the cursor is

The context is then given to one or more *completer* functions which will attempt to complete what you’ve typed.

Each of these completers are tried in order and, if the first one can’t complete the context, the next one will try.
When the context can be completed, some possible _matches_ will be displayed and you can choose whatever you want.

## 🪶 Usage

To initialize the completion for the current session, you need to [[autoload]] the `compinit` function:

```zsh
autoload -U compinit; compinit
```

## ⚙️ Configuration

You can configure many aspects of the completion system using the [[zstyle]] module.

> [!warning]
> Every completion rule defined with `zstyle` should **only** be called after autoloading and calling `compinit`.





[^1]: Sources:
		https://thevaluable.dev/zsh-completion-guide-examples/
