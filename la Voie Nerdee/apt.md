*APT* (stands for *Advanced Package Tool*) is the main command-line package manager for [[Debian]] and its [[Debian derivatives|derivatives]] used to install and manage software [[packages]].

It acts as a front-end for [[dpkg]], automatically resolving complex package dependencies and managing [[apt sources|repositories]].

## 📦 Usage

- Update all the installed packages:

```shell
sudo apt update && sudo apt upgrade 
```

- Remove a package:

```shell
sudo apt remove <package_name>
```

- Remove a package and all its config files:

```shell
sudo apt purge <package_name>
```

## 🪛 Troubleshooting

### Fetch failures

Sometimes apt fails to install or update packages, resulting in a 404 error.
This is usually caused by an interrupted update, mirror rotation or corrupted cache files.

In this case, refreshing package metadata directory may help:

```bash
sudo rm -r /var/lib/apt/lists
```

`apt update` will recreate it on the next run.