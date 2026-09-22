# 🌐 Keyservers

Additional key servers can be specified with the `keyserver` option in the config file:

```bash
# ~/.gnupg/dirmngr.conf
keyserver hkp://keyserver.ubuntu.com
keyserver hkps://keyring.debian.org:443
# etc.
```

# 🔐 Usage

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

>[!warning] Note
>It's recommended to use the long key ID or the full fingerprint when receiving a key. Using a short ID may encounter collisions (see [fake keys found in the wild](https://lore.kernel.org/lkml/20160815153401.9EC2BADC2C@smtp.postman.i2p/) for example)

- Remove key:

```bash
gpg --delete-key <ID>
```

- Verify checksum:

```bash
gpg --verify <signature_file> <source_file>
```

# 🎚️ Trust levels

| *Level*      | *Explanation*                                                                                                    |
| ------------ | ---------------------------------------------------------------------------------------------------------------- |
| **unknown**  | Nothing is known about the owner's judgement in key signing                                                      |
| **none**     | The owner is known to improperly sign other keys                                                                 |
| **marginal** | The owner understands the implications of key signing and properly validates keys before signing them            |
| **full**     | The owner has an excellent understanding of key signing, and his signature on a key would be as good as your own |

- To change trust level:

```bash
gpg --edit-key <ID>
trust
```

# 🪛 Troubleshooting

- If keyrings failed to receive:

```bash
gpgconf --kill dirmngr
```

It'll restart [[dirmngr]] and its config file



[^1]: Sources:
	https://www.gnupg.org/gph/en/manual/x334.html
