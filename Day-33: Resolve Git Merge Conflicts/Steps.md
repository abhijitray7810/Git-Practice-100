# Steps to Fix and Push Changes in Story Blog Repository

1. **SSH into storage server**
   ```bash
   ssh max@ststor01
   ```
Password: Max_pass123

Navigate to the story-blog directory

```bash

cd /home/max/story-blog
```
Check Git status

```bash

git status
```
Open and edit story-index.txt

Ensure it contains titles for all 4 stories.

Correct the typo:

Replace: The Lion and the Mooose

With: The Lion and the Mouse

Save and close the file

Stage and commit changes

```bash

git add story-index.txt
git commit -m "Updated story titles and fixed typo in 'The Lion and the Mouse'"
```
Push changes to the remote repository

```bash

git push origin master
```
If authentication or remote issues occur:

Verify remote URL:

```bash

git remote -v
```
Reset remote URL (if needed):

```bash

git remote set-url origin git@<gitea_server>:sarah/story-blog.git
```
Retry the push command.

Verify changes in Gitea UI

Open Gitea in browser (via top bar “Gitea UI” button).

Login using:

Username: sarah or max

Password: Sarah_pass123 or Max_pass123

Confirm that story-index.txt now shows all 4 titles and the corrected spelling.

(Optional)
Take screenshots or record using loom.com for verification.

yaml

---

Would you like me to include **example content** for `story-index.txt` (with 4 story 
