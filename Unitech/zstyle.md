`zstyle` is a [[Zsh]] built-in command used to configure context-aware settings for shell utilities.

Unlike traditional global shell options (`setopt`) or [[environment variables]], `zstyle` allows you to define styles that only apply under specific *patterns*.

## 📜 Syntax

```zsh
zstyle 'PATTERN' STYLE [values...]
```

Each setting has a *pattern* (also known as *context*), a *style name*, and a *value*.

The _pattern_ act as a namespace. It’s divided by colons `:` and each value between these colons have a precise meaning.

Patterns allow wildcards, so you can set a default one and carve out exceptions:

```zsh
zstyle ':omz:plugins:*' aliases no    # no aliases from any plugin
zstyle ':omz:plugins:git' aliases yes # ...except git
```





[^1]: Sources:
		https://thevaluable.dev/zsh-completion-guide-examples/
