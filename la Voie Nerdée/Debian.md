---
banner: "[[Debian.jpg]]"
banner_icon: 🗻
---
# 🛠️ Installation

1. [Download](https://www.debian.org/distrib/) an ISO and [[GnuPG|verify]] the checksum
2. Check ISO filehash:

```bash
sha512sum --check --ignore-missing <sum_file> # same for sha256sum, md5sum etc.
```

3. [[💿 dd|Create]] the installation medium
4. Disable secure boot
5. Configure [[sudo]]
*(Only if you set a root password during the installation process)*
