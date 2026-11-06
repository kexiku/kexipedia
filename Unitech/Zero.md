In [[Bash]], *zero* (`$0`) is a special read-only variable that stores the path of a [[Processes|process]] used to invoke the current [[shell]] or script.

Its value depends on the execution context:

- **Inside a script:** expands to the path of the file used to invoke the script
- **Directly in the terminal:** expands to the path of the currently running shell (e.g. `/bin/bash`)

> [!note]
> `$0` variable cannot guarantee the full initial script's path to be returned.
> 
> Use [[BASH_SOURCE]] if the full path is crucial for your use case.
