```bash
ssh sarah@ststor01
cd /usr/src/kodekloudrepos/media-t2q3
git checkout -b xfusion-t2q3
cp /tmp/index-t2q3.html ./
git add index-t2q3.html
git commit -m "Add index-t2q3.html file"
git checkout master
git merge xfusion-t2q3
git push origin master
git push origin xfusion-t2q3
```
