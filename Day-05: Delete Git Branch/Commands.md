# Git Branch Deletion Commands

## Objective
Delete the branch named `xfusioncorp_news` from the Git repository located at `/usr/src/kodekloudrepos/news` on the Storage server in Stratos DC.

---

## Commands Execution

### Step 1: Navigate to Repository Directory

```bash
cd /usr/src/kodekloudrepos/news
```

### Step 2: Verify Current Branch

```bash
git branch
```

This command will display all local branches. The current branch is marked with an asterisk (*).

### Step 3: Check Branch Status (Optional)

```bash
git status
```

This shows the current state of your working directory and staging area.

### Step 4: Switch to Different Branch

If you're currently on `xfusioncorp_news`, switch to another branch:

```bash
git checkout main
```

Or if your default branch is master:

```bash
git checkout master
```

### Step 5: Delete the Branch

**Option A - Safe Delete (if merged):**

```bash
git branch -d xfusioncorp_news
```

**Option B - Force Delete (recommended for test branches):**

```bash
git branch -D xfusioncorp_news
```

### Step 6: Verify Deletion

```bash
git branch
```

Confirm that `xfusioncorp_news` no longer appears in the branch list.

### Step 7: Delete Remote Branch (if exists)

If the branch exists on remote repository:

```bash
git push origin --delete xfusioncorp_news
```

---

## Complete Command Sequence

```bash
cd /usr/src/kodekloudrepos/news
git branch
git checkout main
git branch -D xfusioncorp_news
git branch
```

---

## Command Explanations

| Command | Description |
|---------|-------------|
| `cd /usr/src/kodekloudrepos/news` | Navigate to repository directory |
| `git branch` | List all local branches |
| `git branch -a` | List all branches (local and remote) |
| `git checkout <branch>` | Switch to specified branch |
| `git branch -d <branch>` | Delete branch (safe - only if merged) |
| `git branch -D <branch>` | Force delete branch (even if unmerged) |
| `git push origin --delete <branch>` | Delete branch from remote repository |
| `git status` | Show working tree status |

---

## Expected Outputs

### When listing branches:
```
$ git branch
* main
  xfusioncorp_news
  feature-1
```

### When switching branches:
```
$ git checkout main
Switched to branch 'main'
```

### When deleting branch successfully:
```
$ git branch -D xfusioncorp_news
Deleted branch xfusioncorp_news (was a1b2c3d).
```

### After deletion verification:
```
$ git branch
* main
  feature-1
```

---

## Troubleshooting

### Error: Cannot delete checked out branch
```
error: Cannot delete branch 'xfusioncorp_news' checked out at '/usr/src/kodekloudrepos/news'
```
**Solution:** Switch to a different branch first using `git checkout main`

### Error: Branch not fully merged
```
error: The branch 'xfusioncorp_news' is not fully merged.
```
**Solution:** Use force delete: `git branch -D xfusioncorp_news`

### Error: Branch not found
```
error: branch 'xfusioncorp_news' not found.
```
**Solution:** Check branch name spelling or list all branches with `git branch -a`

---

## Important Notes

- You cannot delete the branch you are currently on
- Use `-d` for safe delete (only merged branches)
- Use `-D` for force delete (any branch, regardless of merge status)
- For test branches, force delete (`-D`) is typically appropriate
- Deleting a local branch does not delete it from remote repositories
- Always verify branch deletion with `git branch` after execution

---

## Quick Reference Card

```bash
# Navigate to repo
cd /usr/src/kodekloudrepos/news

# List branches
git branch

# Switch branch
git checkout main

# Delete branch (force)
git branch -D xfusioncorp_news

# Verify
git branch

# Delete from remote (if needed)
git push origin --delete xfusioncorp_news
```

---

## Post-Deletion Checklist

- [ ] Navigated to `/usr/src/kodekloudrepos/news`
- [ ] Verified current branch location
- [ ] Switched away from `xfusioncorp_news` branch
- [ ] Executed delete command
- [ ] Confirmed branch deletion with `git branch`
- [ ] Deleted remote branch (if applicable)
- [ ] Repository remains in working state

---

## Additional Commands for Reference

### View commit history:
```bash
git log --oneline
```

### View all branches with last commit:
```bash
git branch -v
```

### View merged branches:
```bash
git branch --merged
```

### View unmerged branches:
```bash
git branch --no-merged
```

### Restore deleted branch (if SHA known):
```bash
git checkout -b xfusioncorp_news <commit-sha>
```

### Find deleted branch commit SHA:
```bash
git reflog
```
