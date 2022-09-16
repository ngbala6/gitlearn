Working Area                  Staging               HEAD(Local Repo)         Remote Repo

         ------------------------>>-------------------->>------------------------>>

              git add .              git commit -m "msg"   git push origin master

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
git reset --hard 78b976c177ddfa46e996d03c36b899f597a71824


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

git merge 78b976c177ddfa46e996d03c36b899f597a71824 (can merge particular commit)

If conflict is occuring when merge, 

git pull --rebase origin master    (it will give the conflict files)

git mergetool (helps to solve the problem)

#### copy everything exact from one branch to another
git checkout bala (need to update)

git checkout master . (updating master to current branch bala)

git checkout head (checkout to HEAD)

#### Git logs
git log  (help to view logs of commits, get sha and reset to the certain commit)

git log --oneline (give one line answer)

git log --stat  (give full info about files)

git log --patch  (gives full info about files and location)

#### Git Rebase
git rebase similar to git merge

Git Merge -> branch commits get merged to "master" as a single one

Git Rebase -> It takes the history of branch commits & updated in commit msg too(track the changes commit history)

Example: I have 3 commits in "bala" branch and I want to merge in "master" with tracking commits

git checkout master

git rebase bala

git add .

git commit -m "final commit"

git push origin master

#### Git Reflog
It is similar to the "git log"

Where "git log" takes the log of remote repo

"git reflog" takes the entire log of local repo

#### git cherry-pick
Cherry picking in Git means choose a single commit from one branch and apply it in another.

git cherry-pick commit_hash

#### Git Revert
Moreover, we can say that git revert records some new changes that are just opposite to previously made commits. It can be useful for tracking bugs in the project. It make the new commit that is reverted back

If you want to remove something from history then git revert is a wrong choice. try git reset

git revert commit_hash

#### Git Restore
Restore files from Staging & working area

git restore --staged filename.txt (this will restore to prev ver on staging area to working direc)

git restore filename.txt (this will restore to previous version/before modification)

git restore --source commit_hash (restore to particular commit)