*Backports* in [[apt]] are recompiled packages from [[Debian releases|testing]], adjusted and recompiled for usage on Debian stable.

They provide a simple way to use newer software on a stable release without upgrading the entire OS.

> [!warning]
> Backports aren't tested as extensively as Debian stable packages and may cause conflicts with other system components.
> Use with care!

##  🛠️ Setup

- [[apt#Upgrading to the new format|Convert]] your apt source files to a new format if you didn't already
- Create `/etc/apt/sources.list.d/debian-backports.sources`:
```bash
Types: deb deb-src
URIs: http://deb.debian.org/debian
Suites: trixie-backports # if your current version is Debian 13
Components: main contrib non-free non-free-firmware
Enabled: yes
Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg
```
- Run `apt update`

## 📦 Usage

All backports are deactivated by default.

- To install something from backports:
```bash
apt install <package>/trixie-backports
```

- If you also want missing dependencies to be installed from backports too:
```bash
apt install -t trixie-backports <package>
```





[^1]: Sources:
	https://wiki.debian.org/Backports
	https://backports.debian.org/
	https://backports.debian.org/Instructions/
