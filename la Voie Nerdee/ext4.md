*ext4* (*Fourth Extended File System*) is the primary journaling [[file system]] used by most [[Linux]] distributions.

It was developed as a successor to [[ext3]] with an improved design, better performance, and additional features like journal checksumming and delayed allocation.

## 🏷️ Inodes

The number of [[inodes]] In ext4 is determined at the stage of a new file system formatting.

The larger the *bytes-per-inode* ratio, the fewer inodes will be created.

By default, ext4 uses a ratio of one inode every 16384 bytes (16 KiB).

## 💽 Usage

> [!note]
> To manage ext4 partitions, you need to install the `e2fsprogs` package, which contains the required CLI tools

- Format a partition as ext4:

```bash
sudo mkfs.ext4 /dev/<partition>
```





[^1]: Sources:
		https://wiki.archlinux.org/title/Ext4
