---
cssclasses:
  - dashboard
obsidianUIMode: preview
banner: zsh.webp
banner_y: 12.8%
banner_icon: 💤
---
- zsh
	- [[Zsh config]]
	- [[Path modifiers]]
	- [[fpath]]
	- [[autoload]]
	- [[zstyle]]

## 🛠️ Set up

1. Make zsh the default shell:

```bash
chsh -s $(which zsh)
```
*Make sure that zsh is in your authorized shells list (`/etc/shells`)*

2. Log out/in to restart the default shell
3. Test that it worked:

```bash
echo $SHELL # Expected `/bin/zsh` or similar
```

	
