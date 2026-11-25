# SE_LAB_EXTERNAL
This is the set-6 of 2nd question
<br>
Use git commands, git push, pull, fetch, branch, revert, reset, and merge conflict 
git --version
pwd
ls
ls -a
git status
git log --oneline
git branch
git remote -v
clear

git clone https://github.com/varuntejgare/SE_LAB_EXTERNAL.git
cd SE_LAB_EXTERNAL

git config --global user.name "varuntejgare"
git config --global user.email "thisisfridayboss@gmail.com"

gh auth login
gh auth switch --hostname github.com --user varuntejgare
gh auth setup-git
gh auth statusd

echo "Hello Git" > demo.txt
git status
git add demo.txt
git diff --staged
git commit -m "First commit"

echo "Learning Git" >> demo.txt
git diff
git add .
git diff --staged
git commit -m "Updated demo file"

git remote -v
git add .
git commit -m "My changes"
git push origin main

git fetch origin
git status
git log --oneline HEAD..origin/main
git merge origin/main

git pull origin main

git branch
git branch feature
git switch feature
git switch main
git switch -c new-feature
git branch -a
git branch -m renamed-feature
git branch -d feature
git branch -D feature

git switch -c upload-feature
echo "Feature added" > feature.txt
git add .
git commit -m "Added feature"
git push -u origin upload-feature

git switch main
git merge upload-feature
git status
git log --oneline --graph --all

git switch main
echo "Original content" > conflict.txt
git add conflict.txt
git commit -m "Created conflict file"

git switch -c conflict-feature
echo "Feature branch content" > conflict.txt
git add conflict.txt
git commit -m "Updated from feature"

git switch main
echo "Main branch content" > conflict.txt
git add conflict.txt
git commit -m "Updated from main"

git merge conflict-feature

git add conflict.txt
git commit -m "Resolved merge conflict"
git status
git log --oneline --graph --all

git log --oneline
git revert HEAD
git status
git log --oneline

# RESET COMMANDS - RUN ONLY ONE WHEN NEEDED
# git reset --soft HEAD~1
# git reset --mixed HEAD~1
# git reset --hard HEAD~1

git restore demo.txt
git restore --staged demo.txt
git status

git stash
git stash list
git stash apply
git stash pop
git stash drop
git stash clear

git push origin --delete upload-feature
git fetch --prune
git branch -a

git status
git pull origin main
git switch -c my-practical
echo "My Git practical" > practical.txt
git add .
git diff --staged
git commit -m "Completed Git practical"
git log --oneline
git push -u origin my-practical

git status
git log --oneline --graph --all
git branch -a
git remote -v
