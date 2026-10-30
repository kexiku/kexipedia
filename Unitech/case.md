The [[Bash]] `case` statement is a powerful [[Conditional statements|conditional]] control structure used to compare a single value against multiple patterns.

It is a cleaner, more readable alternative to complex `if/elif/else` [[if|chains]]

## 📜 Syntax

```bash
case EXPRESSION in
  PATTERN_1) # Commands to execute if EXPRESSION matches PATTERN_1
  ;;   
  PATTERN_2|PATTERN_3) # Commands to execute if EXPRESSION matches PATTERN_2 or PATTERN_3
  ;;
  *) # Default catch-all
  ;;
esac
```

Key Structural Rules:

- `)`: Terminates the pattern description and begins the command block
- `|`: Matches multiple values in a single clause (acting like an `OR` [[Logical operators|operator]])
- `;;` Serves as a break statement
- `*)` Acts as a catch-all default branch if no other patterns match