Conditional expressions in [[Bash]] are used by the `[[` compound command and the `[`builtin command to test file attributes and evaluate conditions, returning an [[exit status]] of `0` for true and non-zero for false.

## 📄 File expressions

- True if file exists:

```bash
[[ -e ${file} ]]
```

> [!warning]
> While `-a` and `-e` are equivalent in Bash, it's strongly recommended to always use `-e` instead of `-a`.
> 
> The `-a` option has been deprecated and can cause syntax confusion, as it also serves as the logical "AND" operator inside single brackets (`[ ... ]`).
> 
> `-e` complies with [[POSIX]] standards, making your scripts significantly more portable across different shells.

- True if file exists and is a directory file:

```bash
[[ -d ${file} ]]
```

- True if file exists and is a regular file:

```bash
[[ -f ${file} ]]
```

- True if file exists and is a symbolic link:

```bash
[[ -L ${file} ]]
```

- True if file exists and not empty:

```bash
[[ -s ${file} ]]
```

- True if file exists and is readable/writable/executable:

```bash
[[ -[rwx] ${file} ]]
```

- True if file exists and is a symbolic link.

```bash
[[ -L ${file} ]]
```

## 📝 String expressions

True if the length of the string is zero:

```bash
[[ -z ${string} ]]
```

True if the length of the string is non-zero:

```bash
[[ -n ${string} ]]
```

## ❔ Exit status expressions

- True if the command was successful:

```bash
[[ $? -eq 0 ]]
```

- returns true if the command was not successful:

```bash
[[ $? -gt 0 ]]
```





---

<small>Sources:</small>
<small>• https://www.gnu.org/software/bash/manual/html_node/Bash-Conditional-Expressions.html</small>
<small>• https://github.com/bobbyiliev/introduction-to-bash-scripting</small>
