*exFAT* (*Extensible File Allocation Table*) is a lightweight [[file system]] introduced by Microsoft in 2006 to replace the older [[FAT32]] format.

It works natively across modern operating systems, including [[Wimblows]], [[macOS]], [[Linux]] ([[kernel]] 5.4+), Android and iOS.

Unlike [[FAT32]], which caps individual files at 4GB, exFAT supports file sizes up to 16 exabytes and partition sizes up to 128 petabytes, making it ideal for storing large files like high-resolution videos or disk images.

Each exFAT volume uses an allocation bitmap to track the allocation status of clusters, which can help improve performance and reduce fragmentation.

## 💽 Usage

> [!note]
> To manage exFAT partitions in Linux, you need to install the `exfatprogs` package, which contains the required CLI tools

- Format a partition as exFAT:

```bash
sudo mkfs.exfat /dev/<partition>
```





[^1]: Sources:
		https://www.msab.com/glossary/exfat-extended-file-allocation-table/
