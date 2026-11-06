Git stores its settings in text files across three distinct priority levels:

- Repository level (`.git/config`)
- User level (`~/.gitconfig`)
- System level (`/etc/gitconfig`)

Each level overrides values in the previous level, so `.git/config` has higher priority than `~/.gitconfig` and `/etc/gitconfig`.

Here's the overview of all config level options:

| Flag       | Level        | Config location  | Scope                                               |
| ---------- | ------------ | ---------------- | --------------------------------------------------- |
| none       | Repo level   | `.git/config`    | Applies only to the current repo                    |
| `--global` | User level   | `~/.gitconfig`   | Applies to all repos of the current user            |
| `--system` | System level | `/etc/gitconfig` | Applies to every user and every repo on the machine |

## ⚙️ Usage

Git configuration variables can be set using the `git config` command.

👤 Set user name:

```bash
git config --global user.name <your_name>
```

✉️ Set user email:

```bash
git config --global user.email <email@example.com>
```

💻 Set default code editor:

```bash
# For VS Code:
git config --global core.editor "code --wait"
```





---

<small>Sources:</small>
<small>• https://git-scm.com/book/ms/v2/Getting-Started-First-Time-Git-Setup</small>
