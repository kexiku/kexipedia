The `df` (*disk free*) command in [[Linux]] displays information about the disk space usage on the mounted [[file system]].

By default, it shows sizes in raw 1-kilobyte blocks, which can be difficult to read; use `-h` flag to enable human-readable formats.

## 💾 Usage

- Show the disk space usage for the specific directory:

```bash
df <dir>
```

- Display the [[file system]] type in an extra column:

```
df -T
```

- List [[inodes]] information:

```shell
df -i
```