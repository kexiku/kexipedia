The `apt-get` command is a low-level command-line package management tool used to manage software [[packages]] on [[Debian]] and [[Debian derivatives|Debian-based]] Linux distributions.

## ⚔️ apt vs. apt-get

Both `apt` and `apt-get` share the same backend libraries, use the same repositories, and interact with the same package database - however, they cover very different use cases.

`apt` is a high-level tool designed for interactive use and provides human-friendly display output.

`apt-get`, on the other hand, is more oriented towards stable, consistent, and predictable output, making it much more suitable for automation tasks and shell scripting.

Not all that `apt` can do can be done with `apt-get`, as `apt` also includes additional apt commands like `apt-cache`.