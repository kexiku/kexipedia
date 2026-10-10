`zstyle` is a [[Zsh]] built-in command used to configure context-aware settings for shell utilities.

Unlike traditional global shell options (`setopt`) or [[environment variables]], `zstyle` allows you to define styles that only apply under specific *patterns*.

## 📜 Syntax

```zsh
zstyle 'PATTERN' STYLE [values...]
```

Each setting has a pattern (also known as context), a style name, and a value.

Patterns allow wildcards, so you can set a default and carve out exceptions:

```zsh
zstyle ':omz:plugins:*' aliases no    # no aliases from any plugin
zstyle ':omz:plugins:git' aliases yes # ...except git
```