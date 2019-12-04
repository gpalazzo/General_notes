# General_notes
This repository aims to summarize general notes about bash commands and other configuration snippets. It's suppose to be a source for finding useful stuff in a quick and centralized way.

**Please do feel free to suggest both changes in the snippet/description, or adding new snippets/descriptions.**

## SSH
- `Standard TCP SSH port: 22`

### SSH Keys
**Generating SSH key**
  - `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
**"Making" SSH visible to bash**
  - `ssh-agent bash`
**Adding private key to identity file (it allows cloning the repository having the SSH public key)**
  - `ssh-add file_with_private_key`