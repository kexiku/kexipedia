*FAT32* (*File Allocation Table 32*) is a 32-bit [[file system]] developed by Microsoft.

It serves as an updated version of older FAT formats like [[FAT12]] and [[FAT16]] and was the standard file system in Wimblows 95 before [[NTFS]] replaced it in 1993.

FAT32 works across almost all operating systems and devices, including [[Wimblows]], [[macOS]], [[Linux]], gaming consoles, digital cameras, and smart TVs.

The main disadvantage of FAT32 is that a single file stored on a FAT32 drive *cannot* exceed 4 GB, while the maximum partition size is limited to 2 TB.

FAT32 doesn't feature a journaling system, which increases the risk of file corruption if a FAT32-formatted drive is not properly unmounted.

## 💽 Usage

> [!note]
> To manage FAT32 partitions in Linux, you need to install the `mtools` package, which contains the required CLI tools

- Format a partition as FAT32:

```bash
sudo mkfs.vfat -F 32 /dev/<partition>
```

To add a volume label at the same time, include `-n` flag:

```bash
sudo mkfs.vfat -F 32 -n MYLABEL /dev/<partition>
```

- Set the disk image label:

```bash
sudo mlabel -i /dev/<partition> ::MYLABEL
```





[^1]: Sources:
		https://www.coursera.org/articles/fat32
