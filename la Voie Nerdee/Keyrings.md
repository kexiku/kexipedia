*Keyring* is a security feature that stores passwords, [[SSH keys]], [[GnuPG|GPG keys]], and [[certificates]] in encrypted form.

By default keyrings use the user’s login password to unlock. If the login password has changed or auto-login is enabled, they may not unlock automatically.
To fix this, you can update the keyring's password to match your new one.

## 🪛 Troubleshooting

In case you don't remember your previous password and want to reset keyrings:
```bash
# Remove existing keyring
rm ~/.local/share/keyrings/login.keyring && rm ~/.local/share/keyrings/user.keystore
```