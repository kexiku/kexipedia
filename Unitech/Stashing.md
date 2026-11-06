- Take uncommitted changes (both staged and unstaged) and save them for later use:

```bash
git stash
git stash -u # Include untracked files
```

- Reapply last stashed changes:

```bash
git stash pop
```

- Reapply last stashed changes *and* keep them in your stash:

```bash
git stash apply
```

- Remove a single stash:

```bash
git stash drop
```

- Remove all stashes:

```bash
git stash clear
```

- View all stashes:

```bash
git stash list
```

