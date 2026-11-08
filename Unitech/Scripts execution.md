[[Scripts]] in [[Bash]] can be run using different methods:

1. Using the `bash` command:

```bash
bash script.sh
```

2. Using the `sh` command (default shell interpreter):

```bash
sh script.sh
```

3. Running a script as an executable:

```bash
# Set execution permission
chmod +x script.sh

# Run the script (require path)
./script.sh
```

4. [[Source|Sourcing]] a script:

```bash
source ./script.sh
```

Specifying path is optional, but recommended since `source` searches `$PATH` first.

> [!note]
> When a script is sourced, it runs in the current shell environment.
> 
> This means any variables made by the script will persist after the script finishes executing.





---

<small>Sources:</small>
<small>• https://www.geeksforgeeks.org/linux-unix/how-to-run-bash-script-in-linux</small>
