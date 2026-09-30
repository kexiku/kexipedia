`apt autoremove` is an [[apt]] command used in [[Debian derivatives|Debian-based]] Linux distributions to delete packages that were automatically installed as dependencies for other software but are no longer needed.

It checks each [[apt-mark|auto-installed]] package to see if it's required by at least one manually or automatically installed package, and if there are no packages requiring it, it suggests that package for removal.

> [!important]
> `apt autoremove` doesn't make decisions based on whether you actually use the program or how often its binary is run.
> It only sees the dependency tree and the auto/manual flags.

## ♻️ Usage

Using `apt autoremove` is generally safe because it only targets orphan dependencies that no other package explicitly requires.

However, a broken dependency chain or a deleted metapackage can trick apt into deleting critical system applications or an entire [[Desktop environments|DE]].
Using [[apt sources|third-party repositories]] also increases the risk of breaking native package dependency trees.

The fear of removing something important leads many Debian users to fall into a bad habit of not cleaning unused packages at all, resulting in significant amount of digital clutter.

In fact, running `apt autoremove` is virtually risk-free if you follow simple recommendations.

Here are some steps to prevent apt from touching crucial packages:

- Perform a dry run:
```bash
sudo apt -s autoremove
```
This prints exactly what apt plans to remove without making any changes.

 - Analyze the output:
>[!success] Safe to remove
>- Libraries (`lib...`)
>- Old Linux kernels (`linux-image-...`)
>- Headers
- Search the output for crucial packages:
>[!caution] Danger zone
>- Core components
>- Metapackages (`ubuntu-desktop`, `gnome-core`, `gdm3`)
>- Networking tools (`network-manager`)

If you found a package you want to save, you can use `apt-mark` command to explicitly [[apt-mark|mark]] it as manually installed.

Once marked manual, `apt autoremove` will ignore it.

## 📑 Configs

By default, `apt autoremove` doesn't delete configuration files for removed packages.

If you want them to also being removed, use `--purge` flag:
```bash
apt autoremove --purge <package_name>
```

## 🪛 Troubleshooting

If system starts to behave strangely or refuses to boot after running `apt autoremove`, don't panic.

First, open the apt history log to see what exactly was removed:
```bash
less +G /var/log/apt/history.log # read from the end
```
Then, reinstall the missing packages directly from the command line.





[^1]: Sources:
	https://fastfox.pro/blog/tutorials/apt-autoremove-safe-cleanup/