# git-tips-tricks
Repository for me to keep useful tips and tricks for git.

Good tutorial from W3schools:

https://www.w3schools.com/git/default.asp?remote=github

## Create a new branch and switch to it
```
git checkout -b new_branch_name
```
## Switch to an existing branch
```
git checkout branch_name
```
## Merge a branch into the current branch
NB: Remember to pull changes on the branch you are merging from first:
```
git checkout target_branch       # Switch to the branch you want to pull
git pull origin source_branch    # Pull changes from source branch on the remote repository
git checkout your_branch         # Switch back to your branch
```
then:
```
git merge branch_name
```
## Delete gone local branches (linux)

Fetch changes first:
```
git fetch -p
```
Delete branches:
```
git branch -vv | grep ': gone]'|  grep -v "\*" | awk '{ print $1; }' | xargs -r git branch -d
```
## View remote branches
```
git branch -a
```
## Delete branch on remote
```
git push remote_name -d remove_branch_name
```
## Delete branch local
```
git branch -d local_branch_name
```
## Combining multiple commits into a single commit

There are a few ways to achieve this:

- Undo all commits and re-commit just once (Easiest)
- Squash all commits to one (Easier)
- Using rebase (Complex)

## View remote branches
```
git branch -a
```
## Undo last commit (but keep changes)
```
git reset --soft HEAD~1
```
## Undo last commit (and discard changes)
```
git reset --hard HEAD~1
```
## Amend the last commit

If you forgot to add some changes or need to change the commit message
```
git commit --amend
```
## Stash changes

Save changes that are not yet ready to be committed
```
git stash
```
