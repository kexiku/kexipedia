[[Apt]] stores not only the version and dependency list for each package, but also an *installation method*.

A package can be marked as either manually installed or automatically installed. 

When you explicitly install a package with `apt install`, it's usually assigned the **manual** status.
Package's dependencies, such as libraries or modules, are marked as **auto**.

To save an orphan package from being removed with [[apt autoremove]], you can manually mark it as manually installed with `apt-mark` command:

```bash
sudo apt-mark manual <package_name>
```