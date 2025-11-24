Creating and Initializing a Git Repository
```bash
ssh sarah@ststor01
mkdir -p /home/sarah/story-blog-t1q4
cd /home/sarah/story-blog-t1q4
git init
echo "A Lion lay asleep in the forest" > lion-and-mouse-t1q4.txt
git add lion-and-mouse-t1q4.txt
git commit -m "Add lion-and-mouse-t1q4.txt with initial content"
```
