`~/.zshenv`
- Executed for any [[Shell types|type]] of shell invocations
- *Always* starts first
- Suitable for variables that should be available to other programs
    (`$ZDOTDIR`, `$PATH`, etc.)

 `~/.zprofile`
- Executed for any type of *login* shells
- Runs once when you invoke a new shell
- Suitable for [[environment variables]]

`~/.zshrc`
- Executed for any type of *interactive* shells
- Runs every time you open a new terminal window
- Suitable for [[aliases]], [[functions]] and prompt customization





[^1]: Sources:
	https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH
	https://unix.stackexchange.com/questions/71253/what-should-shouldnt-go-in-zshenv-zshrc-zlogin-zprofile-zlogout
	https://batsov.com/articles/2025/03/01/back-to-the-basics-zsh-without-oh-my-zsh/