When building a set of interdependent shell [[scripts]], it becomes crucial to ensure that common scripts do not get accidentally [[source|sourced]] twice.

The solution is actually pretty simple:

```bash
[[ -n "${_UTILS_LOADED:-}" ]] && return || readonly _UTILS_LOADED=1
```

## 🔍 Details

- [[Parameter expansion]] (`:-`)
- [[Conditional expressions]] (`-n`)
- [[Logical operators]] (`&&`, `||`)
- [[readonly]]





---

<small>Sources:</small>
<small>• https://www.coderwall.com/p/it3b-q/bash-include-guard</small>
