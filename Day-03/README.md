# Day 59: Git Repository Cloning on Storage Server

## Objective
Clone an existing Git repository from `/opt/blog.git` to the `/usr/src/kodekloudrepos` directory on the Stratos Data Center Storage Server, using the `natasha` user. 

The task must ensure **no modifications to repository files, directories, or permissions**.

## Environment
- Server: `ststor01` (Stratos DC)
- Repository Path: `/opt/blog.git`
- Target Directory: `/usr/src/kodekloudrepos`
- User: `natasha`

## Learning Outcomes
- Understand cloning a local Git repository.
- Handle "dubious ownership" errors in Git.
- Work safely as a non-root user.
```

---

### **2️⃣ QUESTIONS.md**

```markdown
# Day 59: Questions

1. What command is used to clone a Git repository locally?
2. What does the "dubious ownership" error in Git mean, and why does it occur?
3. How can you clone a repository safely without changing permissions or ownership?
4. Why is it important to not modify repository permissions when multiple teams need access?
5. What is the difference between cloning via SSH and cloning a local path?
```

---

### **3️⃣ COMMANDS.md**

````markdown
# Day 59: Commands to Clone Git Repository Safely

### Step 1: Connect to the Storage Server
```bash
ssh natasha@ststor01
````

### Step 2: Switch to natasha user (if needed)

```bash
sudo su - natasha
```

### Step 3: Navigate to target directory

```bash
cd /usr/src/kodekloudrepos
```

### Step 4: Clone the repository safely without modifying permissions

```bash
GIT_CEILING_DIRECTORIES=/usr/src git -c safe.directory=/opt/blog.git clone /opt/blog.git
```

### Step 5: Verify the repository

```bash
cd blog
git status
```

You should see:

```
On branch main
nothing to commit, working tree clean
```

> ✅ Notes:
>
> * This approach avoids changing repository ownership or permissions.
> * The cloned directory will appear as `blog` inside `/usr/src/kodekloudrepos`.

```


