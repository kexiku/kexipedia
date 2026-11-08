A *shebang* is a character sequence (`#!`) placed on the very first line of [[Unix]]-like [[scripts]] that tells the [[kernel]] which interpreter to use for executing the file.

It ensures script portability and allows scripts to be run as executables without explicitly calling the interpreter.

Examples of shebangs include `#!/bin/bash` for [[Bash]] or `#!/usr/bin/env python3` for [[Python]].

## 📜 Syntax

```
#! /path/to/interpreter [...ARGUMENTS]
```

An interpreter can be either specified using an absolute, hardcoded path, or invoked by the [[env]] utility, in which case the path should be `/usr/bin/env bash`.

For system-critical scripts running with elevated privileges, the first option is more secure, since the interpreter's location cannot be easily manipulated with a custom `$PATH` variable.

> [!info]
> Shebang only works when the file is *executed*.
>
> If the script meant to be [[source|sourced]], the kernel cannot choose the interpreter to run it because no new process is started.





---

<small>Sources:</small>
<small>• https://en.wikipedia.org/wiki/Shebang_(Unix)</small>
