# mac-dev-setup
Development environment setup on macOS


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

## Bugs and Issues
- Python pytest package
  Error: Key Error: Break Loop
  https://stackoverflow.com/questions/35045038/how-do-i-use-pytest-with-virtualenv

- Wrong 'requirements.txt' file gets installed: <br>
  `pip cache purge` <br>
  `pip install --upgrade pip setuptools` <br>
  `pip install --no-cache-dir -r requirements.txt` <br>

