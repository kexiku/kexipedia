## ⚙️ Config

 `~/.bash_profile`
- Executed for [[Shell types#Interactive login shells|interactive login shells]]
- Runs once when you invoke a new shell
- Suitable for [[environment variables]]

`~/.bashrc`
- Executed for [[Shell types#Interactive non-login shells|interactive non-login shells]]
- Runs every time you open a new terminal window
- Suitable for custom [[aliases]] and [[functions]]

`~/.bash_login`
- Fallback for `.bash_profile`
- Exists for historical reasons

`~/.bash_logout`
- The shell cleanup file
- Executed when a login shell exits
- Suitable for running tasks at logout

## ⌨️ Hotkeys

![[moving_cli(1) 1.png]]

| *Command*             | *Meaning*                                       |
| --------------------- | ----------------------------------------------- |
| `←`/`→`               | Move one character back/forward                 |
| `Ctrl + →`/`Ctrl + ←` | Move one word back/forward                      |
| `Ctrl + A`/`Home`     | Go to the beginning of command line             |
| `Ctrl + E`/`End`      | Go to the end of command line                   |
| `Tab`                 | Autocomplete                                    |
| `Ctrl + H`            | Delete the character before cursor              |
| `Ctrl + D`            | Delete the character under the cursor           |
| `Ctrl + U`            | Clear all characters before cursor              |
| `Ctrl + K`            | Clear all characters after cursor               |
| `Ctrl + W`            | Delete the word before the cursor               |
| `Alt + D`             | Delete the word after the cursor                |
| `Ctrl + Y`            | Paste previously deleted characters             |
| `Ctrl + T`            | Swap two characters before cursor               |
| `Alt + T`             | Swap current word with previous                 |
| `Alt + U`             | Uppercase characters from cursor to end of word |
| `Alt + L`             | Lowercase characters from cursor to end of word |
| `Ctrl + C`            | Terminate the current process                   |
| `Ctrl + Z`            | Suspend the current process                     |
| `Ctrl + S`            | Pause the current process                       |
| `Ctrl + Q`            | Resume the current process                      |
| `Ctrl + D`            | Exit shell                                      |





[^1]: Sources:
	https://www.uwyo.edu/data-science/resources/knowledge-base/what-is-a-bash-profile.html
	https://www.baeldung.com/linux/bashrc-vs-bash-profile-vs-profile
