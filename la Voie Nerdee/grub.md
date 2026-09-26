## ⚙️ Config

Grub config is located at `/etc/default/grub` and can be edited with `sudoedit`
> [!tip]
> Don't forget to rebuild the config file after making any changes:
> ```bash
> sudo update-grub # Debian | Ubuntu
> sudo grub-mkconfig -o /boot/grub/grub.cfg # Arch
sudo grub2-mkconfig -o /boot/grub2/grub.cfg # Fedora
> ```

### 🧠 Remember last boot choice
```bash
GRUB_DEFAULT=saved
GRUB_SAVEDEFAULT=true
```

### ⏳ Set timeout
```bash
GRUB_TIMEOUT=5
          # -1 for disable timeout
          #  0 for instant boot
```

### 🖥️ Set display resolution

- Find your screen resolution:
```bash
xdpyinfo | awk '/dimensions/{print $2}'
```
- Edit config file:
```bash
GRUB_GFXMODE=<width>x<height>
```

### 🎨 Install a theme

- Clone theme directory to the `/boot/grub/themes`
- Edit config file (`sudoedit /etc/default/grub`):
```shell
# Path to custom theme
GRUB_THEME="<path_to_your_theme.txt>"
	```
