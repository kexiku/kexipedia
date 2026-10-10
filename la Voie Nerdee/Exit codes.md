An *exit code* (also known as an *status code*) is a numerical value returned by a command or script to indicate the outcome of its execution.

In [[Linux]], code `0` generally indicates a successful result; anything other than `0` is considered an error.

> [!warning]
> In many programming languages, this is exactly the opposite: zero is considered "false" and nonzero values are considered "true"

The `?` [[environment variables|environment variable]] contains info about the exit status of the previous command.