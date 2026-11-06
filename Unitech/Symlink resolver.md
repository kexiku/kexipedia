```bash
SCRIPT_PATH="$(readlink -f "${BASH_SOURCE[0]}")"
SCRIPT_DIR="${SCRIPT_PATH%/*}"

source "$SCRIPT_DIR/lib/helpers.sh"
source "$SCRIPT_DIR/lib/config.sh"
# etc.
```

## 🔍 Details

1. [[BASH_SOURCE]]
2. [[readlink]]
3. [[Command substitution]] (`$()`)
4. [[Parameter expansion]] (`%/*`)
5. [[source]]
