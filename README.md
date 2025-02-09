# Git Commands

## Git config

### See Config

To see the configuration of the Git

```bash
git config --list
```

### Set User

#### For Global

This means it will use this user details through out your pc

```bash
git config --global user.name 'Your Name'
git config --global user.email 'Your Email'
```

#### For Local

This means it will use this user details only in that specific folder

```bash
git config --local user.name 'Your Name'
git config --local user.email 'Your Email'
```

## Initaliziting Repository

To initialize a repository `git init` command is used to create a repo with `master` or `main` branch.
This will also create a folder called `.git` to track all the changes in your working folder. To delete the repo the `.git` folder can be deleted

## Git Status and Git Ignore

To check the changes of your folder use `git status` to check the status of your file.

If you want to avoid some files from being tracked create a file called `.gitignore` and the filename in the `.gitignore` file.

## Stagging

To Stage the files before commiting use

```bash
git stage .
```

To Stage only a specific file use

```bash
git stage filename
```

To Reset the staged file use

```bash
git reset .
```

## Git Commit

To commit the stages use

```bash
git commit -m "commit message"
```

To log the commit information use

```bash
git log
```

## Git Remote

To check if the git is connected to any remote repository use

```bash
git remote
git remote -v
git remote show origin
```

To add a remote repo use

```bash
git remote add origin repository_url
```

## Git Push

To Push the repository to remote

```bash
git push origin main
git push origin main -u
```

The `-u` flag in the `git push origin main -u` command stands for `--set-upstream`. When you use this flag, Git sets the specified branch (`main` in this case) as the upstream branch for the current local branch. This means that in future interactions, Git will know which remote branch to interact with by default, allowing you to simply use commands like `git push` or `git pull` without needing to specify the branch each time.

## Fetch and Merge

To get the file from remote repo use

```bash
git fetch
```

This will only get the files from the remote repo and it will affect the local repo. To merge both repo use

```bash
git merge origin/main
```

## Git Pull

To avoid git `fectch` and `merge` you can use

```bash
git pull origin main
```

or if the upstream branch is set, you can use

```bash
git pull
```

## Git clone

To clone a repository with all its previous commits and log use

```bash
git clone repository_url
git clone repository_url folder_name
```

You can also specify the folder name to clone the repo

## Git Branch

To create a branch use

```bash
git branch awesome
```

To list the branches

```bash
git branch
```

To rename the branch

```bash
git branch -M rename
```

To delete the branch

```bash
git branch -d awesome
git branch -D awesome
```

## Git Checkout

To move from one branch to another use

```bash
git checkout awesome
```

To create and checkout at same time use

```bash
git checkout -b awesome
```

Added in master
Added in awesome

## Git Merge

To merge branches commit and checkout to the desired branch and merge.

```bash
git checkout main
git merge awesome
```

If there is a conflict you can accept both changes.

## Git Reset

If a file is changed and it is staged, but if you want to unstage it you can use

```bash
git rest
```

If you have commit it and reset the commit, get the commit id from the log and reset with the id.

```bash
git reset commit_id
```

This reset the commit but the changes will be in the unstaged state. If to move to the previous commit without the changes use

```bash
git reset --hard commit_id
```

## Git Revert

Unlike the reset which deletes the commit, revert go back to the previous commit with out deleting the recent commit and creating a new commit from the recent commit.

```bash
git revert commit_id
```

## Git Amend

To add info to the existing commit or to add the unstaged file we can use `git commit --amend`.

To change the commit message

```bash
git commit --amend -m "better message"
```

To add the unstaged file to the existing commit use

```bash
git add .
git commit --amend --no-edit
```

This will add the changes to the existing commit.

## Git Stash

Stash is a command in git that lets to save the command in a seperate list that wont appear in the commit and also when the code is pushed to the remote server. The stash is used as `git stash`. To restore the stash `git stash pop`

But to have the multiple stash we can name the stash

```bash
git stash save post1
```

To list the stash we can use the command

```bash
git stash list
```

To restore the one of the stash from the list use the index id given the stash list command

```bash
git stash apply 1
```
