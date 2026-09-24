---
banner: systemd.webp
banner_icon: 🎛️
---
## 🔧 Manage

Set default boot target:
```bash
sudo systemctl set-default multi-user.target # boot into CLI (text mode)
sudo systemctl set-default graphical.target # boot into GUI (display manager)
```
