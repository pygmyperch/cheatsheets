# Quick Start: Create and Push a New Repository
*Last updated: November 27, 2024*

This guide walks through creating a new repository locally and pushing it to GitHub.

## Local Setup

1. Create and navigate to your project directory:
```bash
mkdir my-new-project
cd my-new-project
```

2. Initialize the Git repository:
```bash
git init
```

3. Create a README.md file:
```bash
echo "# My New Project

Brief description of your project.

## Getting Started

Instructions for setting up and using your project.

## Features

List of key features.

## Contributing

How others can contribute to your project.
" > README.md
```

4. Create a .gitignore file:
```bash
# MacOS system files
.DS_Store

# Editor directories
.vscode/
.idea/

# Language-specific
__pycache__/
*.pyc
.Rhistory
.RData

# Environment directories
venv/
env/
.env

# Build directories
build/
dist/
" > .gitignore
```

5. Add and commit the files:
```bash
git add README.md .gitignore
git commit -m "Initial commit: Add README and .gitignore"
```

## GitHub Setup

1. Create a new repository on GitHub:
   - Go to https://github.com/new
   - Enter repository name
   - Do NOT initialize with README, .gitignore, or license
   - Click "Create repository"

2. Connect local repository to GitHub:
```bash
git remote add origin https://github.com/username/my-new-project.git
```

3. Push your code:
```bash
git branch -M main
git push -u origin main
```

## Verify Setup

1. Check repository status:
```bash
git status              # Should show "nothing to commit"
git remote -v          # Should show your GitHub repository
```

2. Visit your GitHub repository URL to confirm the files are there.

## Next Steps

1. Add project files
2. Create development branches
3. Set up project documentation
4. Add license if needed
5. Configure branch protection (optional)

## Common Issues

1. If push fails with "remote origin already exists":
```bash
git remote rm origin
git remote add origin https://github.com/username/my-new-project.git
```

2. If push is rejected:
```bash
git pull origin main --allow-unrelated-histories
git push origin main
```