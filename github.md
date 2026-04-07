## Local-Remote relationship

### Show state of synchronization between local and remote repository

`git remote show origin`

### List all branches

`git branch -a`

### Download remote repository info (branches, history etc)

`git fetch origin`

### Let git figure out the remote origin/HEAD

`git remote set-head origin -a`

### Change local-branch- to-remote-branch relationship

`git branch --set-upstream-to=origin/${remote_b_name} ${local_b_name}`

`git branch -u origin/${remote_b_name} ${local_b_name}`

## Local branches

### Create new branch from current

`git checkout -b ${new_local_b_name}`

### Change from current branch to another one

`git switch ${other_b_name}`

### Rename local branch

`git branch -m ${from_b_name} ${to_b_name}`

### Remove local branch

`git branch -D ${local_b_name}`

## Remote branches

### Push changes to remote branch

`-f` - forcefully, in case of `git commit --amend`

`git push [-f] origin ${remote_b_name}`

### Remove remote branch

`git push origin --delete ${remote_b_name}`

### Copy remote branch and switch to it

`git checkout [--track] [-b ${local_b_name}] [origin/]${remote_b_name}`

`git checkout --track -b ${local_b_name} origin/${remote_b_name}`

`git checkout -b ${local_b_name} origin/${remote_b_name}`

`git checkout ${remote_b_name}`

or in 2 steps:

`git fetch origin ${local_b_name}:${remote_b_name}`

`git checkout ${local_b_name}`

## Local file tracking

### Add

`git add ${path_to_a_file_or_folder}`

`git add --all`

### Remove

`-r` recursively for folders

`-f` force

`git rm --cached ${path_to_a_file_or_folder} [-rf]`

## Local commits

### Create new commit with message

`git commit -m ${message}`

### Override last commit

`git commit --amend`

### Remove last X commits

`--soft` to leave code changes but remove the commit

`--hard` to remove both code changes and the commit

`git reset --[hard/soft] HEAD~${commit_amount}`

`git reset --[hard/soft] origin master`

### Change current branch history to start from other local branch

`git rebase ${local_b_name_to_start_off_from}`

#### resolve all conflicts

`git rebase --continue`

#### fail rebase

`git rebase --abort`

## Tags

### List

`git tag`

### Sync with tag

`git switch --detach ${tag_name}`

### Delete tag

`git tag -d ${tag_name}`