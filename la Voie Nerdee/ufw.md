*Uncomplicated Firewall (ufw)* is a user-friendly command-line tool used to manage netfilter firewall rules on Linux distributions.

It uses [[iptables]] as a backend.

## 🛠️ Setup

- Install the package:
```bash
sudo apt install ufw
```

> [!warning]
> If you are configuring over SSH, you may wish to allow SSH before enabling the firewall (see the guide below).
> 
> If your connection gets interrupted before allowing SSH you may be locked out of your system.

- Enable firewall:
```bash
sudo ufw enable
```

- Set up default config:
```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

- Verify that the firewall is enabled:
```bash
sudo ufw status verbose
```

## 🚔 Rules

By default ufw denies all of the incoming connections, which will make it a problem if you are using SSH.
Therefore, you must create a rule which allows SSH connections:
```bash
sudo ufw allow ssh
```

Other rules may be added in the same way by simply specifying a name of the program.

Ufw comes with preloaded defaults for some commonly used software.
To list the default apps:
```bash
sudo ufw app list
```

Rules may be deleted with the following command:
```bash
sudo ufw delete allow ssh
```





[^1]: Sources:
	https://wiki.debian.org/Uncomplicated%20Firewall%20%28ufw%29
