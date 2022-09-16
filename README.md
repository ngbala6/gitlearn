#### Create branch
git branch newbranch oldbranch

or git branch newbranch


#### Delete branch in remote
git push origin --delete branch-name

#### Delete branch in local
git branch -D branch name

#### Rename branch in local
git branch -m old_branch new_branch
or
git branch -m newname

#### Renamed branch affect in remote
git push origin :oldbranch

git push origin newbranch

#### Switch branch
git checkout branch_name /git switch branch_name


Adding .gitignore
create .gitignore and add *.ipynb. this will remove all *.ipynb files when git add

#### Give helpful info
git status

#### Get updated remote branches when its deleted
git fetch --prune

#### Reset the local changes to remote
git reset --hard <sha>

#### Git commit. . . help when you committed mistakenly without adding an other file
git add bala.py
git commit -m "adding bala.py"
git add he.py
git commit --amend -m "adding he.py too"
git push origin master

#### rm file
git rm bala.py
git mv bala.py src/gold.py (move files)

#### Merge files from one branch to other
git checkout bala
git merge master    --> (this merges master branch to bala)

#### copy everything exact from one branch to another
git checkout bala (need to update)
git checkout master . (updating master to current branch bala)
