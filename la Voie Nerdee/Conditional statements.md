Very often, we want to run a certain command only if a certain *condition* is met.

For example, we might want to run the command `cp source.txt destination.txt` if, and only if, `source.txt` exists.

In [[bash]], we can do that like this:

```bash
if [[ -e source.txt ]] then
  cp source.txt destination.txt
fi
```

The construction `[[ CONDITION ]]` contains a [[File test operators|test conditional expression]] which returns an [[Exit codes|exit status]] of zero (*success*) if `CONDITION` is true, and a non-zero exit status (*failure*) if `CONDITION` is false.

In our case, `CONDITION` is `-e source.txt`, which is true if and only if there exists a file named `source.txt`.

If we want to use an arbitrary command status as a conditional, we need to add a semicolon after the command to demarcate it from the `then`:

```bash
if grep -q needle haystack.txt; then
  echo Found the needle!
fi
```

## If statements

`if` statement allows to specify multiple commands to run if the conditional expression succeeds.

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
