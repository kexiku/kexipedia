```bash
TEMP_DIR="" # Temporary files directory
BG_PID="" # Backgroud process PID

cleanup() {
	# Capture the original exit status before it's being overwritten
	local exit_code=$?
	
	# Kill background jobs
	if [[ -n "$BG_PID" ]] && kill -0 "$BG_PID" 2>/dev/null; then
		kill "$BG_PID" 2>/dev/null || true
	fi

    # Remove temporary files
    if [[ -n "$TEMP_DIR" && -d "$TEMP_DIR" ]]; then
	    rm -rf -- "$TEMP_DIR"
	fi
	
	# Exit with previously captured status
	exit "$exit_code"
}

# Catch an EXIT signal
trap cleanup EXIT

# --- Main script ---
TEMP_DIR=$(mktemp -d)
# ...
```

## 🔍 Details

1. [[trap]]
2. [[PID]]
3. [[Question mark]] (`$?`) | [[Exit status]]
4. [[Conditional statements]]
5. [[Conditional expressions]] (`-n`, `-d`)
6. [[Logical operators]] (`&&`, `||`)
7. [[kill]]
8. [[Redirection]] (`2>`)
9. [[Error suppression]] (`|| true`)
10. [[Double dash]] (`--`)
11. [[mktemp]]
12. [[Command substitution]] (`$()`)