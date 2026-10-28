An *inode* (short for *index node*) is a data structure in [[Linux]] [[file system]] that stores metadata about a [[Files|file]] or directory, such as size, permissions, owner, and timestamps.
Each inode points to the disk blocks where the file data is stored.

Inodes don't contain file names - they are stored separately in file directories.

Creating a new file, directory, symlink etc. requires at least *one* free inode.
If the inode count is too low, no file can be created on the file system even though there is still space left on it.

> [!warning]
> It's not possible to change either the bytes-per-inode ratio or the inode count after the file system is created

Typically about 1% of the total disk space is reserved for the inode table.

## 🏷️ Usage

- List all the inodes:

```shell
df -i
```



[^1]: Sources:
		https://wiki.archlinux.org/title/Ext4
