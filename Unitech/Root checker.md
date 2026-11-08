```bash
check_root () {
  if [[ $EUID -ne 0 ]]; then
    echo "This script must be run as root."
    exit 1
  fi
}
```

## 🔎 Details

1. [[EUID]]
2. [[Comparison operators]] (`-ne`)
3. [[echo]]
