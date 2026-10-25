`trap` is a [[Bash]] buitin that can handle asynchronous [[signals]] and execute commands in response to them.

It's commonly used to clean up temporary files, manage errors, and makes script exit gracefully on interruption.

## 📜 Syntax

```bash
trap 'commands' SIGNAL_1 SIGNAL_2 ...
```

### 'commands'

- The string of code to run when the signal is caught

### SIGNAL

- The specific Unix [[Signals|signal]] that triggers the trap
- Can be specified by name (e.g. `SIGINT`) or by value (e.g. `2`)

## 📢 Signals

| Signal         | Description                                                |
| -------------- | ---------------------------------------------------------- |
| `SIGINT (2)`   | Interrupt (typically sent when pressing Ctrl+C)            |
| `SIGTERM (15)` | Termination (often used for stopping processes gracefully) |
| `SIGKILL (9)`  | Kill (forcefully terminates a process)                     |
| `SIGTSTP (20)` | Stop (sent by pressing Ctrl+Z)                             |
| `EXIT (0)`     | A pseudo-signal received when the script exits             |

> [!warning]
> `SIGKILL (9)` cannot be trapped, caught, or ignored.
> The operating system kills or pauses the process immediately.





[^1]: Sources:
		https://www.geeksforgeeks.org/linux-unix/shell-scripting-bash-trap-command/
