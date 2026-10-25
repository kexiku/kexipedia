### `~/.zshenv`

- Executed for any [[Shell types|type]] of shell invocations
- *Always* starts first
- Suitable for variables that should be available to other programs
    (`$ZDOTDIR`, `$PATH`, etc.)

###  `~/.zprofile`

- Executed for any type of *login* shells
- Runs once when you invoke a new shell
- Suitable for [[environment variables]]

### `~/.zshrc`

- Executed for any type of *interactive* shells
- Runs every time you open a new terminal window
- Suitable for [[aliases]], [[functions]] and prompt customization

> [!info]
> By default, Zsh will try to find the user’s configuration files in the `$HOME` directory.
> 
> You can change this behavior by setting the `$ZDOTDIR` environment variable in `.zshenv` file.
> 
> *(Important: `.zshenv` file itself needs to be placed in your home directory!)*





[^1]: Sources:
	https://thevaluable.dev/zsh-install-configure-mouseless/
	https://unix.stackexchange.com/questions/71253/what-should-shouldnt-go-in-zshenv-zshrc-zlogin-zprofile-zlogout
	https://batsov.com/articles/2025/03/01/back-to-the-basics-zsh-without-oh-my-zsh/
	