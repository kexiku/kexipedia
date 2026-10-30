The `set` command is a [[Bash]] builtin used for controlling the behavior of the script.

It allows to modify shell options, configure environmental attributes, and handle positional parameters.

## 📑 Options

### `-e`

- Exit immediately if a command returns non-zero status

### `-u`

- Treat unset variables as errors instead of empty strings

### `-o pipefail`

- Stop the script if any of the piped command fails
- Set the script's [[Exit status codes|status code]] to the rightmost non-zero status code in a [[Pipelines|pipeline]]

> [!tip]
> The common use case of `set` is enabling the "Bash Strict Mode":
> ```bash
> set -euo pipefail
> ```
> Putting this line at the beginning of the script makes it much easier to debug, causing the execution to fail loudly and explicitly on most unpredictable errors.






[^1]: Source:
		https://www.geeksforgeeks.org/linux-unix/shell-scripting-set-command/
		https://linuxize.com/post/bash-strict-mode/
		https://linuxcommandlibrary.com/man/set
