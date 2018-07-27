# git-cheatsheet

A cheatsheet of Git commands.

- [cd, ls](#terminal-navigation)
- [git init, git config](#git-setup)
- [status, log](#state-checking)
- [editor](#git-editor)
- [git remote](#remote-branch)
- [git add, git commit](#add-and-commit)
- [delete local and remote branch](#delete-local-and-remote-branch)

## terminal navigation
```bash
# navigate to a particular folder
cd "<path>"
# navigate up a folder
cd ..
# navigate to your home folder
cd
# list items in current folder
ls
```

## git setup
```bash
# initialize a git repository
cd "<desired-path>"
git init
# check global and local git settings
git config --global -l
git config --local -l
# configure global git settings
git config --global user.name "<full-name>"
git config --global user.email "<email>"
git config --global core.editor "nano -w"
# configure local git settings
cd "<desired-path-for-local-settings>"
git config --local user.name "<local-full-name>"
git config --local user.email "<local-email>"
```

## state checking
```bash
# check git status
git status
# check git log
git log                # verbose
git log --oneline      # condense each commit to a single line
git log --oneline -n 5 # print only the last 5 commits
```

## remote branch
```bash
# view remote settings
git remote -v
# configure 'origin' remote branch
git remote add origin <https-origin-url>
# change 'origin' remote branch URL
git remote set-url origin <https-origin-url>
# configure 'upstream' remote branch (when working with a fork)
git remote add upstream <https-origin-url>
# change 'upstream' remote branch URL
git remote set-url upstream <https-origin-url>
```

## add and commit
```bash
# stage one file
git add <file.ext>
# stage all files (danger, this stages all changes)
git add .
# commit with message
git commit -m "Message"
```

## delete local and remote branch
```bash
# delete local branch only if its commits are merged upstream
git branch -d <local-branch-name>
# delete local branch unconditionally
git branch -D <local-branch-name>
# delete remote branch
git push origin :<remote-branch-name>
```

## useful workflows
```bash
# sync a fork with an upstream repository
git fetch upstream
git checkout master
git merge upstream/master
# sync a branch with new changes made in master
git fetch origin
git checkout <branch-name>
git merge origin/master
```
