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
