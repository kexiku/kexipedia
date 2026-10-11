Very often, we want to run a certain command only if a certain *condition* is met.

For example, we might want to run the command `cp source.txt destination.txt` if, and only if, `source.txt` exists.

In [[bash]], we can do that like this:

```bash
if [[ -e source.txt ]] then
  cp source.txt destination.txt
fi
```

The construction `[[ CONDITION ]]` contains a [[File test operators|test conditional expression]] which returns an [[Exit status codes|exit status]] of zero (*success*) if `CONDITION` is true, and a non-zero exit status (*failure*) if `CONDITION` is false.

In our case, `CONDITION` is `-e source.txt`, which is true if and only if there exists a file named `source.txt`.

If we want to use an arbitrary command status as a conditional, we need to add a semicolon after the command to demarcate it from the `then`:

```bash
if grep -q needle haystack.txt; then
  echo Found the needle!
fi
```





[^1]: Sources:
		https://en.wikibooks.org/wiki/Bash_Shell_Scripting/Conditional_Expressions
		https://www.w3schools.com/bash/bash_conditions.php
