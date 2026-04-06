### Show state of synchronization between local and remote repository

`git remote show origin`

### List all branches

`git branch -a`

### Download remote repository info (branches, history etc)

`git fetch origin`

### Let git figure out the remote origin/HEAD

`git remote set-head origin -a`

### Rename local branch

`git branch -m ${from_b_name} ${to_b_name}`

### Push changes to remote branch

`-f` - forcefully, in case of `git commit --amend`

`git push -f origin ${remote_b_name}`

### Change local branch - to - remote branch relationship

`git branch --set-upstream-to=origin/${remote_b_name} ${local_b_name}`

`git branch -u origin/${remote_b_name} ${local_b_name}`

### Remove remote branch

`git push origin --delete ${remote_b_name}`