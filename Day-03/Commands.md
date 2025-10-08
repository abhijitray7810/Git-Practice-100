# Day 59: Commands to Clone Git Repository Safely

### Step 1: Connect to the Storage Server
```bash
ssh natasha@ststor01
```
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
pgsql

On branch main
nothing to commit, working tree clean
```
✅ Notes:

This approach avoids changing repository ownership or permissions.

The cloned directory will appear as blog inside /usr/src/kodekloudrepos.

```yaml

---
