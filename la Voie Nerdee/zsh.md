## ⚙️ Config

`~/.zshenv`
- Executed for any [[Shell types|type]] of shell invocations
- *Always* starts first
- Suitable for variables that should be available to other programs
    (`$PATH`, `$EDITOR`, etc.)

 `~/.zprofile`
- Executed for any type of *login* shells
- Runs once when you invoke a new shell
- Suitable for [[environment variables]]

`~/.zshrc`
- Executed for any type of *interactive* shells
- Runs every time you open a new terminal window
- Suitable for [[aliases]], [[functions]] and prompt customization

## 🛠️ Set up

- Make zsh the default shell:

```bash
chsh -s $(which zsh)
```
*Make sure that zsh is in your authorized shells list (`/etc/shells`)*

- Log out/in to restart the default shell
- Test that it worked:

```bash
echo $SHELL # Expected `/bin/zsh` or similar
```





[^1]: Sources:
	https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH
	https://unix.stackexchange.com/questions/71253/what-should-shouldnt-go-in-zshenv-zshrc-zlogin-zprofile-zlogout
