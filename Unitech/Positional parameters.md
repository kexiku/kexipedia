*Positional parameters* in [[Bash]] provide a way to access value of the first parameter supplied when executing the script or function.

- `$0`: the name or path used to invoke the current script
- `$1`: the first argument
- `$2`: the second argument
- ...
- `${10}`: the tenth argument (*double-digit parameters require curly braces*)

> [!tip]
> To extract the script's basename from its path, use the following syntax:
> ```bash
> ${0##*/}
> ```
> `##` removes the longest matching prefix that matches the pattern following it, while `*/` matching any sequence of characters ending with `/`.
> 
> Together, `${0##*/}` removes all the characters before the last slash, leaving only the final path component (the script file).





[^1]: Sources:
		https://bash.cyberciti.biz/guide/$1
