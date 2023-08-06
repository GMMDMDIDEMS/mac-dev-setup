# mac-dev-setup
Development environment setup on macOS


## Homebrew
Install homebrew

## iTerm
Install iTerm, don't use `warp`!

Setup iTerm with zsh: `oh-my-zsh`.
Add `.zshrc` file

## Starship
https://starship.rs/

## Terminal


- `cat <file>`: concatenate and display the contents of one or multiple files


## Visual Studio Code Setup

Via command palette:
---
1. To open repo via terminal with `code .`:
   
Shell Command: Install 'code' command in PATH
`command": "workbench.action.installCommandLine`

2. Controls whether entires in .gitignore should be parsed and excluded from the explorer.
`"explorer.excludeGitIgnore": true`

3. Open repository via integrated vscode terminal in the same window
`code -r .`

## Git

Clean-up if files were committed to repo before using .gitignore file: <br>
`git rm -r --cached .` <br>
`git add .` <br>
`git commit -m 'repo clean-up` <br>
`git push` <br>


`git show <id>` <br>
`git log -p` <br>
`git log --stat` <br>
`git diff` <br>
`git add -p` <br>
`git checkout <file>` - git checkout restores files to the latest stored snapshot, reverting any changes before staging.<br> 
`git reset HEAD <file>` - remove changes from the staging area <br>
`git commit --amend` - modify and add changes to the most recent commit. Only for local changes, because will change git history!!! <br>
`git branch` - list branches <br>
`git branch <branch_name>` - create new branch <br>
`git checkout <existing_branch>` <br>
`git checkout -b <new_branch>` <br>
`git branch -d <branch>` - delete branch <br>
`git merge <branch>` - merges branch with current branch <br>
`git log -p origin/master` <br>
`git log --graph --oneline --all` <br>
`git remote -v` <br>
`git rebase <branch>` <br>
`git push --delete origin <branch>` - delete after succesfull merge <br>
`git rebase -i <master>`



Rollback
`git revert HEAD` - new commit is created with inverse changes. This cancels previous changes instead of making it as though the original commit never happened. <br>
`git revert <commit_id>`

Delete and rename files
`git rm <file>`
`git mv <old_file> <new_file>`

- Undo `git init`:
  `rm -rf .git`



## Python
Setup venv:
`python3 -m venv env`

Activate venv:
`source env/bin/activate`

## Bugs, Issues and Fixes
- Python pytest package <br>
  Error: Key Error: Break Loop <br>
  https://stackoverflow.com/questions/35045038/how-do-i-use-pytest-with-virtualenv

- Wrong `requirements.txt` file gets installed: <br>
  `pip cache purge` <br>
  `pip install --upgrade pip setuptools` <br>
  `pip install --no-cache-dir -r requirements.txt` <br>


## Upcoming Content Updates and Expansion
- Editing Text Files With Vi (https://www.howtogeek.com/102468/a-beginners-guide-to-editing-text-files-with-vi/)
- https://github.com/nicolashery/mac-dev-setup#visual-studio-code
- How to share (vscode, python, terminal) settings between different devices
