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

* navigate to a particular folder
```bash
cd "<path>"
```

* navigate up a folder
```bash
cd ..
```

* navigate to your home folder
```bash
cd
```

* list items in current folder
```bash
ls
```

## git setup

* initialize a git repository
```bash
cd "<desired-path>"
git init
```

* check global and local git settings
```bash
git config --global -l
git config --local -l
```

* configure global git settings (cd anywhere)
```bash
git config --global user.name "<full-name>"
git config --global user.email "<email>"
git config --global core.editor "nano -w"
```

* configure local git settings
```bash
cd "<desired-path-for-local-settings>"
git config --local user.name "<local-full-name>"
git config --local user.email "<local-email>"
```

## state checking

* check git status
```bash
git status
```

* check git log
```bash
git log                # too verbose
git log --oneline      # condenses to a single line
git log --oneline -n 5 # prints only the last 5 commits
```

## git editor

* check editor version and run
```bash
nano --version
nano # exit nano with Ctrl-X
vim --version
vim
emacs --version
emacs
```

## remote branch
```bash
git remote -v
# the remote branch is named origin in this example
git remote add origin <https-origin-url>
git remote set-url origin <https-origin-url>
```

## add and commit
```bash
# add
git add <file.ext>
git add . # danger, this stages all changes
# commit
git commit -m "Message"
```

## delete local and remote branch
```bash
git branch -D <local-branch-name>
git push origin :<remote-branch-name>
```
