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

### Initaliziting Repository

To initialize a repository `git init` command is used to create a repo with `master` or `main` branch.
This will also create a folder called `.git` to track all the changes in your working folder. To delete the repo the `.git` folder can be deleted

### Git Status and Git Ignore

To check the changes of your folder use `git status` to check the status of your file.

If you want to avoid some files from being tracked create a file called `.gitignore` and the filename in the `.gitignore` file.

### Stagging

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
