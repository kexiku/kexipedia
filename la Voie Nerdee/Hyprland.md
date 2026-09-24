---
banner: "[[Hyprland.webp]]"
banner_icon: 💧
---
## ⚙️ Setup
### Enable Dark theme for GTK (GNOME apps):
```bash
gsettings set org.gnome.desktop.interface color-scheme 'prefer-dark'

sudo pacman -S adw-gtk3
gsettings set org.gnome.desktop.interface gtk-theme 'adw-gtk3-dark'

gsettings get org.gnome.desktop.interface color-scheme # To check
```
- Install xsettingsd (lightweight GNOME settings faker):
```bash
sudo pacman -S xsettingsd
```
- Create `~/.config/xsettingsd/xsettingsd.conf`:
```bash
Net/ThemeName "adw-gtk3-dark"
Gtk/ColorScheme "prefer-dark"
```
- AutoStart it in Hyprland:
```bash
# ~/.config/hypr/hyprland.conf
exec-once = xsettingsd &
```
