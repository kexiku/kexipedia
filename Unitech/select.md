The `select` construct in [[Bash]] is a built-in feature used to generate interactive [[Menu|menus]] in scripts.

It displays a numbered list of options and prompts user to make a selection.

## ☑️ Usage

In most cases, `select` is used in conjunction with a [[case]] statement and the special `PS3` variable to customize the prompt.

Options for `select` are typically stored in [[arrays]], but can also be a series of string variables or a single string with space-separated words:

```bash
select ITEM in [...OPTIONS]
```

If the user enters a number that corresponds to one of the items in the `OPTIONS`, then the value of `ITEM` is set to that item.

The exact raw input the user typed is stored in the special `$REPLY`variable.

> [!info]
> The `select` loop will continue to run and prompt the user for input until the `break` command is executed, so make sure to include it in all the options

## 📋 Example menu

```bash
# Customize the prompt
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





---

<small>Sources:</small>
<small>• https://linuxize.com/post/bash-select</small>
