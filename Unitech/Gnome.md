---
banner: "[[gnome.webp]]"
banner_icon: 🐾
banner_y: 68.4%
---
## ⚙️ Set up

### ⌨️ Change layout switching shortcut

```bash
$ gsettings set org.gnome.desktop.wm.keybindings switch-input-source "['<Shift>Alt_L']"
$ gsettings set org.gnome.desktop.wm.keybindings switch-input-source-backward "['<Alt>Shift_L']"
```

### 📂 Set Files shortcut

- Go to Settings > Keyboard > View and Customize Shortcuts
- Custom Shortcuts
- Create a shortcut with this command:

```bash
nautilus --new-window
```

### 🚫 Disable annoying Emoji shortcuts

- Run `ibus-setup`
- Go to Emoji tab
- Clear Emoji annotation shortcuts

### Disable extensions auto-download

```bash
gsettings set org.gnome.software download-updates false
```

### 🪄 Download & Install incompatible extensions

```bash
gsettings set org.gnome.shell disable-extension-version-validation true
```

### ⛅ Reset weather locations

```bash
gsettings reset org.gnome.Weather locations
```