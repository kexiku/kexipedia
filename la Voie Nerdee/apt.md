*APT* (stands for *Advanced Package Tool*) is the main command-line package manager for [[Debian]] and its [[Debian derivatives|derivatives]] used to install and manage software [[packages]].

It acts as a front-end for [[dpkg]], automatically resolving complex package dependencies and managing [[apt sources|repositories]].

## 🪛 Troubleshooting

### Fetch failures

If apt refuses to install/update a package due to 404 error, refreshing package information cache may help:
```bash
sudo rm -r /var/lib/apt/lists
```
`sudo apt update` will recreate the lists directory on the next run.