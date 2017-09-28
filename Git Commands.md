# Git Commands

## Remove all your local git branches but keep master
git branch | grep -v "master" | xargs git branch -D

## Create a new branch BASED ON THE CURRENT BRANCH
git checkout -b <newBranch>
 
## Undo all local pending changes
git reset HEAD --hard
 
## Undo a single file change
git checkout -- <fileName>
 
## Push new branch to server
git push origin <branchName>
 
## Delete remote branch
git push origin --delete <branchName>
 
## List all local and remote branches
git branch -a
 
## Remove deleted branches
git remote prune origin
 
## Pull remote master branch and merge it into current branch
git pull origin master
 
## Undo last commit but keep files (before it's pushed)
git reset HEAD~1
 
## Rename current branch to new name
git branch -m <newname>
 
## Save temporarily your changes so you can check out another branch
git stash
 
## List temporary saves
git stash list
 
## Get back changes from a temporary save
git stash apply
 
## Delete temporary saves
git stash drop
 
## Rename local branch
git branch -m <newname>

## Amend Your Last Commit
git commit --amend

## See Changed Files Between Branches
git diff --name-only <branch>