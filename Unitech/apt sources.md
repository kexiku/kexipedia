[[Apt]] downloads and installs packages from one or more software *repositories*, sometimes called *sources*.

Common apt repositories include [[Debian releases|Stable]], Security and [[Backports]].

Adding repositories lets you manage non-Debian packages using normal Debian package management tools, making them easy to update and remove.

> [!warning]
> Adding third-party repositories can [[Don't break Debian|break your system]] in ways that are hard to fix

## ⚙️ Config

The main apt sources configuration file is `/etc/apt/sources.list.d/debian.sources`

If you add a new source, it's best to create a separate file for it: put it in the same directory with a name that describes the source and ends with `.sources`
(e.g. `/etc/apt/sources.list.d/vscode.sources`)

## 📝 Formats

Old `sources.list` files should be converted to the modern `debian.sources` format (recommended to use since [Trixie](https://wiki.debian.org/DebianTrixie))

- To upgrade sources files, run:

```bash
sudo apt modernize-sources
```

## 📑 Structure

### ❔ Types

The `Type` field says what is in the repository:

- **deb** indicates that the archive contains normal binary packages (`.deb`)
- **deb-src** indicates source packages (`.dsc`)

### 🌐 URIs

The address of the repository

### 💿 Suites

Usually the codename of a release, like `bookworm` or `sid`
Can also be an alias like `stable`, `testing` or `unstable`

### 📦 Components

One or more parts of the repository.
You can limit the set of components if you don't want your system to use packages from specific categories like `non-free` for non-[DFSG](https://wiki.debian.org/DebianFreeSoftwareGuidelines)-compliant software

### ✒️ Signed-By

[[Keyrings|Keyring]] using for verifying packages.

## 📚 Examples

For a working configuration with all suites and components enabled, see:

- `/usr/share/doc/apt/examples/debian.sources`





[^1]: Sources:
		https://wiki.debian.org/SourcesList
