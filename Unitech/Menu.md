```bash
# Customize the menu prompt
PS3="Choose an option (1-3): "

# Define menu options in an array
options=("Install" "Update" "Quit")

# Start the select loop
select opt in "${options[@]}"; do
    case $opt in
        "Install")
            echo "Installing..."
            # ... logic ...
            break
            ;;
        "Update")
            echo "Updating..."
            # ... logic ...
            break
            ;;
        "Quit")
            break
            ;;
        *) 
            echo "Invalid option."
            ;;
    esac
done
```

## 🔍 Details

1. [[select]]