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

Configuration: https://starship.rs/config/ <br> 
Emojis: https://emojipedia.org/
command+control+space

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
`git rebase -i <master>` <br>
`git diff --cached` - to check files after they've been added with `git add `

Delete braches locally and remote: <br>
https://stackoverflow.com/questions/2003505/how-do-i-delete-a-git-branch-locally-and-remotely

Update/sync remote repository: <br>
https://stackoverflow.com/questions/7244321/how-do-i-update-or-sync-a-forked-repository-on-github

Pipreqs UniDecodeError:
`pipreqs . --ignore "env_name"`

PR steps
1. Check `git remote -v`
2. New branch: `git checkout -b "new_branch_name"`
3. `git remote add upstream https://github.com/original_author/original_repo_name`
4. `git push -u origin <new branch>`
   
Find a project you want to contribute to
Fork it
Clone it to your local system
Make a new branch
Make your changes
Push it back to your repo
Click the Compare & pull request button
Click Create pull request to open a new pull request

### Update PR Fork
https://stackoverflow.com/questions/7244321/how-do-i-update-or-sync-a-forked-repository-on-github

### Discard unstaged changes
https://stackoverflow.com/questions/52704/how-do-i-discard-unstaged-changes-in-git




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

### Pyenv, Poetry
pyenv shell 3.8.12
poetry env use python3.8
poetry install

## Conda
Setup env and create `.yml` file: https://stackoverflow.com/questions/51042589/conda-version-pip-install-r-requirements-txt-target-lib
Conda cheatsheet: https://conda.io/projects/conda/en/latest/_downloads/843d9e0198f2a193a3484886fa28163c/conda-cheatsheet.pdf

## Mamba-Forge
https://github.com/Paradoxdruid/mamba-how-to



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
- `pyenv` (https://blog.teclado.com/how-to-use-pyenv-manage-python-versions/) vs `virtualenv`
- `pipreqs` vs `pip freeze` (https://github.com/bndr/pipreqs)
- `mamba-forge` vs `conda-forge` vs `miniforge`
- add `ssh` commands
- [Number of lines in github repository](https://stackoverflow.com/questions/26881441/can-you-get-the-number-of-lines-of-code-from-a-github-repository)
- [How to import requirements.txt from an existing project using Poetry](https://stackoverflow.com/questions/62764148/how-to-import-requirements-txt-from-an-existing-project-using-poetry)
- shell script to unpack and delete all .zip files within a folder
- [How can I find what is taking up the space?](https://askubuntu.com/questions/911865/no-more-disk-space-how-can-i-find-what-is-taking-up-the-space)