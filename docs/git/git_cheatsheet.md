# Git Operations Guide
*Last updated: November 27, 2024*

This guide covers common Git operations and commands for version control. It serves as a quick reference for both basic and advanced Git usage.

## Table of Contents
- [Basic Operations](#basic-operations)
- [Branch Management](#branch-management)
- [Remote Operations](#remote-operations)
- [Undoing Changes](#undoing-changes)
- [Advanced Operations](#advanced-operations)
- [Configuration](#configuration)
- [Best Practices](#best-practices)

## Basic Operations

Initialize and clone repositories:
```bash
# Initialize a new repository
git init

# Clone an existing repository
git clone https://github.com/username/repository.git

# Clone a specific branch
git clone -b branch-name https://github.com/username/repository.git
```

Track and commit changes:
```bash
# Check status of your files
git status

# Add files to staging
git add filename.txt    # Add specific file
git add .              # Add all files

# Commit changes
git commit -m "Your commit message"
git commit -am "Add and commit in one step"  # Only works for modified files
```

## Branch Management

Work with branches:
```bash
# List branches
git branch              # Local branches
git branch -r           # Remote branches
git branch -a           # All branches

# Create and switch branches
git branch branch-name
git checkout branch-name
git checkout -b new-branch    # Create and switch in one command

# Delete branches
git branch -d branch-name     # Local branch
git push origin --delete branch-name  # Remote branch
```

## Remote Operations

Manage remote repositories:
```bash
# Add remote repository
git remote add origin https://github.com/username/repository.git

# View remote repositories
git remote -v

# Push changes
git push origin main
git push -u origin main    # Set upstream for first push

# Get latest changes
git fetch origin
git pull origin main
```

## Undoing Changes

Fix mistakes:
```bash
# Discard changes in working directory
git checkout -- filename.txt
git restore filename.txt      # New Git syntax

# Unstage files
git reset filename.txt
git restore --staged filename.txt    # New Git syntax

# Undo last commit (keep changes)
git reset --soft HEAD~1

# Undo last commit (discard changes)
git reset --hard HEAD~1
```

## Advanced Operations

More complex tasks:
```bash
# Stash changes
git stash
git stash list
git stash pop

# Cherry-pick commits
git cherry-pick commit-hash

# Interactive rebase
git rebase -i HEAD~3    # Rebase last 3 commits

# Create and apply patches
git format-patch -1 HEAD
git am < patch-file.patch
```

## Configuration

Set up Git:
```bash
# Set user info
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Set default branch name
git config --global init.defaultBranch main

# List all configurations
git config --list
```

## Best Practices

- Write clear, descriptive commit messages
- Commit early and often
- Pull before pushing to avoid conflicts
- Create branches for new features
- Keep main/master branch stable
- Use .gitignore for files that shouldn't be tracked
- Regularly fetch and merge upstream changes

## Related Resources

- [Official Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com)
