# Git previous commit completely remove from GitHub

### 1. Identify the Commit to Delete
```bash
git log
```

### 2. Use git rebase to Remove the Commit
```bash
git rebase -i <commit-hash>
```

### 2.1 Change pick to **drop**
If you're using Vim:
```bash
Press Esc to exit insert mode.
Type :wq and hit Enter to save and quit.
```

If you're using Nano:
```bash
Press Ctrl + X, then Y to confirm saving, and press Enter.
git push origin <branch-name> --force
```

### 3. Force Push the Changes
```bash
git push origin <branch-name> --force
```

---

### Alternative: Use git reset (for Local Repos)
```bash
git reset --hard <commit-hash>
```
