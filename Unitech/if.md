`if` statement in [[Bash]] allows to specify multiple commands to run if the [[Conditional statements|conditional expression]] succeeds.

in addition, we can use `else` clause to specify one or more commands to run instead if the conditional expression fails:

```bash
if [[ -e source.txt ]] then
  echo 'source.txt exists; copying to destination.txt.'
  cp source.txt destination.txt
else
  echo 'source.txt does not exist; exiting.'
  exit 1 # terminate the script with a nonzero exit status (failure)
fi
```

To check multiple conditions in sequence, we can use `elif` ("else-if") statements:

```bash
if [ $num -gt 10 ]; then
  echo "Number is greater than 10"
elif [ $num -eq 10 ]; then
  echo "Number is exactly 10"
else
  echo "Number is less than 10"
fi
```

A single `if` statement can have any number of `elif` clauses, representing any number of fallback conditions.

To run a command only if a condition is false, we can use the `!` [[Logical operators|operator]].

For example, the following statement will copy `source.txt` to `destination.txt` unless `destination.txt` already exists:

```bash
if ! [[ -e destination.txt ]] then
  cp source.txt destination.txt
fi
```





[^1]: Sources:
		https://en.wikibooks.org/wiki/Bash_Shell_Scripting/Conditional_Expressions
		https://www.w3schools.com/bash/bash_conditions.php
