# Git Useful Command

## Git Basic Command

```Bash
# Init your repo
git init you_proj_dir
# Clone repo from remote
git clone your_remote_repo.git
# Stash your change
git add . # Stash all files
git add your_file
# Commit your change
git commit
git commit --amend # Use last commit
git commit -m "Your Message"
# Push commited code to remote
git push
# Get commit log
git log
```

## Config Your Git
```Bash
# Change to your Github E-Mail and user name
git config --local/global user.email "you@example.com"
git config --local/global user.name "Your Name"
# List your config
git config --local/global -l
```