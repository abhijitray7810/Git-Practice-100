## 🚀 Option 3 (Best): Use SSH (no login ever again)

### Step 1: Generate SSH key

```bash
ssh-keygen -t ed25519 -C "royabhijits928@gmail.com"

```

### Step 2: Start SSH agent

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

### Step 3: Add key to GitHub

```bash
cat ~/.ssh/id_ed25519.pub
```

Copy and paste into GitHub Dashboard(main) → Settings → SSH & GPG key → Paste → SSH keys

---

### Step 4: Change remote URL

```bash
git remote set-url origin git@github.com:abhijitray7810/aegis-stack.git
```

---

### Step 5: Test

```bash
ssh -T git@github.com
```

---

## ⚠️ Important Note

You’re using:

```bash
git push origin main --force
```

This can overwrite history and cause data loss. Use it only if you understand the risk.

---
