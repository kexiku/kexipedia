---
banner: "[[Debian.webp]]"
banner_icon: 🗻
cssclasses:
  - dashboard
---
## 🛠️ Installation

For the minimal, least-bloated setup:

1. [Download](https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/) the netinst ISO, the checksum file and the matching `.sign` file
2. Download the Debian public key [manually](https://www.debian.org/CD/verify) (you need a 2011-01-05 version)
   or use `wget`:
```bash
wget -c "https://www.debian.org/CD/key-DA87E80D6294BE9B.txt"
```
4. Import the downloaded key to keyring:
```bash
gpg --import key-DA87E80D6294BE9B.txt

gpg --list-keys # check the result
```
5. [[GnuPG#🔐 Usage|Verify]] the checksum file
6. Check ISO filehash:
```bash
sha512sum --check --ignore-missing <sum_file> # same for sha256sum, md5sum etc.
```
7. [[dd|Create]] the installation media
8. Boot from the media and follow the installer steps
9. On the "Partition disks" menu, make sure to create all the required partitions properly

- Example of Debian partition scheme for dual-boot setup:
```
╭─────────────────────────────────────────────────────────────────────────╮
| ID  |  Size     | Flag | FS    |  Description                   | Mount |
|-------------------------------------------------------------------------|
| #1  |  200 MB   |  K   |  ESP  |  Basic data partition          |       |
| #2  |  16.8 MB  |      |       |  Microsoft reserved partition  |       |
| #3  |  250.0 GB |      |  ntfs |  Basic data partition          |       |
| #4  |  250.0 GB |  f   |  ext4 |                                |  /    |
| #5  |  4.0 GB   |  f   |  swap |                                | swap  |
╰─────────────────────────────────────────────────────────────────────────╯
```
10. When you get to "Software selection", deselect everything but System Utilities
11. After reboot:
```bash
sudo apt update && sudo apt install gnome-core -y && sudo apt purge ifupdown -y && sudo shutdown -r now
```
You will need to remove the ifupdown package (used by installer) to avoid conflict with NetworkManager (used by Gnome)

12. Edit the NetworkManager config:
```bash
# /etc/NetworkManager/NetworkManager.conf
<...>

[ifupdown]
managed=true # make sure it set to 'true'
```
13. Reboot
14. Enjoy your system ❤️

## 💡 Bonus steps:

- Install [[Flatpak]]
- Install additional packages:
```bash
sudo apt install fonts-noto freefilesync git gpg gnome-shell-extension-manager gnome-tweaks imagemagick pipx python3-pip python3-venv seahorse stow ufw unifont wget yt-dlp zsh zsh-syntax-highlighting -y
```

[[Debian releases]]


[^1]: Sources:
	https://www.reddit.com/r/debian/comments/14ykux3/comment/jrsuowc/?utm_source=share&utm_medium=web3x&utm_name=web3xcss&utm_term=1&utm_content=share_button
