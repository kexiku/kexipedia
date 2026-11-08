In [[Bash]], *zero* (`$0`) is a special read-only variable that stores the path of a [[Processes|process]] used to invoke the current [[shell]] or script.

Inside a [[source|sourced]] file, `$0` still holds the name of the script that did the sourcing, not the file being read. That makes `$0` unreliable for extracting a sourced file's location.

Bash keeps the actual file path in the [[BASH_SOURCE]] array instead, where `BASH_SOURCE[0]` is the path of the file currently being executed.
