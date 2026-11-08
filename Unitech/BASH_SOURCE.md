`BASH_SOURCE` is an internal array variable in [[Bash]] that contains the source filenames corresponding to the elements in the execution call stack.

Unlike the standard [[Zero|$0]] variable, which always points to the initial [[Processes|process]] name, `${BASH_SOURCE[0]}` evaluates to the path of the currently executed script, regardless of whether the file was run directly or [[Source|sourced]].

Thus, the [[Zero|$0]] variable in a sourced `script.sh` file will contain the current [[shell]] executable name (e.g. `/bin/bash`), while the value of `${BASH_SOURCE[0]}` will always be `script.sh`.

It's commonly used to [[Source directory resolver|find the absolute path to the script directory]].
