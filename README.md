# mac-dev-setup
Development environment setup on macOS

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