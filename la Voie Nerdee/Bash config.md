### `~/.bash_profile`
 
- Executed for [[Shell types#Interactive login shells|interactive login shells]]
- Runs once when you invoke a new shell
- Suitable for [[environment variables]]

### `~/.bashrc`

- Executed for [[Shell types#Interactive non-login shells|interactive non-login shells]]
- Runs every time you open a new terminal window
- Suitable for custom [[aliases]] and [[functions]]

### `~/.bash_login`

- Fallback for `.bash_profile`
- Exists for historical reasons

### `~/.bash_logout`

- The shell cleanup file
- Executed when a login shell exits
- Suitable for running tasks at logout





[^1]: Sources:
	https://www.uwyo.edu/data-science/resources/knowledge-base/what-is-a-bash-profile.html
	https://www.baeldung.com/linux/bashrc-vs-bash-profile-vs-profile