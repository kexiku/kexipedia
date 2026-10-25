In Unix-like operating systems, a *hostname* (commonly called *short hostname*) is the label assigned to a system to identify it.

It helps the [[kernel]] and user [[processes]] to distinguish the host system from other ones.

The hostname is set during the installation and usually stored in `/etc/hostname` file.

## 🏠 Usage

- View hostname:

```bash
hostname
```

- Change hostname:

```bash
sudo hostnamectl set-hostname <new_hostname>
```

> [!tip]
> It's recommended to also update the hosts file after changing the hostname:
> 
> ```bash
> # in /etc/hosts
> 127.0.0.1	localhost
> 127.0.1.1	<new_hostname>
> ```





[^1]: Sources:
		https://wiki.debian.org/Hostname?pow_referer=https%3A%2F%2Fwww.google.com%2F
