`chkdsk` (*Check Disk*) is a built-in [[Wimblows]] utility that scans hard drive for file system errors and bad sectors.

## 🔧 Drive repair steps

1. Backup important files
2. Check [[SMART]] status (use tools like [CrystalDiskInfo](https://crystalmark.info/en/software/crystaldiskinfo/))
3. Run as Administrator:

```powershell
chkdsk <drive_letter> /r # locate bad sectors and recover readable data
```

> [!important]
> `chkdsk` cannot repair disks when they're mounted.
> 
> If the command above is refuses to execute, try to run it from the [[Wimblows Recovery Environment]]



