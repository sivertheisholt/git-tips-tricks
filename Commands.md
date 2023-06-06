# Git commands

## Delete gone local branches

Fetch changes first:

git fetch -p

Delete branches:

git branch -vv | grep ': gone]'|  grep -v "\*" | awk '{ print $1; }' | xargs -r git branch -d

## View remote branches

git branch -a

## Delete branch on remote

git push remote_name -d remove_branch_name

## Delete branch local

git branch -d local_branch_name
