```bash
SOURCE_DIR="$(cd -- "$(dirname -- "${BASH_SOURCE[0]}")" && pwd)"
```

## 🔍 Details

1. [[BASH_SOURCE]]
2. [[dirname]]
3. [[Double dash]] (`--`)
4. [[Command substitution]] (`$()`)
5. [[cd]]
6. [[Logical operators]] (`&&`)
7. [[pwd]]

> [!tip]
> To get the script directory with symlinks resolved, use [[realpath]] command:
>```bash
>SOURCE_DIR="$(dirname -- "$(realpath -- "${BASH_SOURCE[0]}")")"
>```

