*GnuPG* (*GNU Privacy Guard*) is a command-line tool that lets you encrypt and sign your data.

It's often used to verify software integrity and authenticity.

## 🏠 Home

GnuPG uses its own directory to store [[keyrings]], private keys and config files. 
The default path for GnuPG home directory is `~/.gnupg`.

## ⚙️ Config

GnuPG checks `~/.gnupg/gpg.conf` for user's configuration.

The file doesn't exist by default: to use it, you must create it and set its [[permissions]] to `600`

The config file supports any GnuPG command line options.

Each option needs to be written at the new line in `<option> <arguments>` format *(without the two dashes)*

## 🌐 Keyservers

Additional key servers can be specified with the `--keyserver` option.
To specify them permanently, add them to the config file:

```bash
keyserver hkp://keyserver.ubuntu.com
keyserver hkps://keyring.debian.org:443
# etc.
```

## 🔏 Usage

- List keys:

```bash
gpg --list-keys
```

- Import key:

```bash
# From a remote keyserver
gpg --recv-keys 0x<long_ID>

# From a local file
gpg --import <key_file>
```

It's recommended to use the long key ID or the full fingerprint when receiving a key. Using a short ID may encounter collisions (see [fake keys found in the wild](https://lore.kernel.org/lkml/20160815153401.9EC2BADC2C@smtp.postman.i2p/) for example)

- Remove key:

```bash
gpg --delete-key <ID>
```

- Verify a file:

```bash
gpg --verify <signature_file> <source_file>
```

- Change the key's [[Ownertrust|trust level]]:

```bash
gpg --edit-key <key_ID>
trust
```

## 🪛 Troubleshooting

- If a keyserver failed to receive, try to restart [[dirmngr]]:

```bash
gpgconf --kill dirmngr
```





[^1]: Sources:
	https://www.gnupg.org/gph/en/manual/x334.html
	https://wiki.archlinux.org/title/GnuPG
