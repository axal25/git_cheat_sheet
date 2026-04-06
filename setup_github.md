# Setup GitHub

## Initial setup

`git config --global user.email ${email@address.com}`

`git config --global user.name ${user_name}`

`git config --global init.defaultBranch master`

## SSH Keys

### Check usual location for existing keys

`ls -la ~/.ssh`

### Generate new key

`ssh-keygen -t ed25519 -C "${email@address.com}"`

### Run SSH Agent

`eval "$(ssh-agent -s)"`

### Add SSH key on local machine

`ssh-add ~/.ssh/${id_ed25519}`

### Change authorization method to SSH

`git remote set-url origin git@github.com:${user_name}/${repository}.git`

example: 

`git remote set-url origin git@github.com:axal25/CV.git`

### Add SSH key to GitHub

`cat ~/.ssh/${id_ed25519}.pub`

Copy into

[Settings > Access > SSH and GPG keys > New SSH key](https://github.com/settings/keys)

### Verify SSH Auth

`ssh -T git@github.com`

```text
Hi axal25! You've successfully authenticated, but GitHub does not provide shell access.
```
