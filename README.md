# General_notes
This repository aims to summarize general notes about bash commands and other configuration snippets. It's suppose to be a source for finding useful stuff in a quick and centralized way. Reminder: it's only commands for unix system (I can't guarantee it works in Windows).

**Please do feel free to suggest both changes in the snippet/description, or adding new snippets/descriptions.**

## SSH
- `Standard TCP SSH port: 22`

#### SSH Keys
##### Generating SSH key
  - move to `~/.ssh/` and then `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
##### "Making" SSH visible to bash
  - `ssh-agent bash`
##### Adding private key to identity file (it allows cloning the repository having the SSH public key)**
  - `ssh-add file_with_private_key`

## Package installation
#### All statements below refer to the same thing, even though `pip` and `conda` might have differences in terms of packages they can install
- `pip install -r path_to_requirements.txt` or
- `conda install --yes --file requirements.txt` or
- `while read requirement; do conda install --yes $requirement; done < requirements.txt`

## Working with paths
#### Find file path
Replace "pattern" with a filename or matching expression, such as "*.txt" (Leave the double quotes in).
- `find . -name "pattern" -print`

## GitHub
##### Track file history (logs) in a repository
- `git log --all --full-history -- <path_to_file>` (without <>)

##### Steps to clear history of github repository
1. move to the repository you want to perform the action
2. `rm -rf .git`
3. `git init`
4. `git add .`
5. `git commit -m "commit_message"` (substitute commit_message for the message you want)
6. `git remote add origin git@github.com:<YOUR ACCOUNT>/<YOUR REPOS>.git` (note you would need ssh permission for this action)
7. `git push -u --force origin master`
