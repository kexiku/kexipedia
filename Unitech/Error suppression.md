## 💬 Suppress error message

[[Redirection|Redirect]] all [[Standard streams|standard errors]] to `/dev/null`:

```bash
command 2>/dev/null
```

## ✅ Allow failures on `set -e`

SInce `true` always returns `0`, it can be used to prevent script from exiting in [[strict mode]] (`set -e`) by setting the final [[exit status]] of a [[pipeline]]:

```bash
command 2>/dev/null || true
```
