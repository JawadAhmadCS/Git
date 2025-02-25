# Git Notes

## 1. Introduction to Git
Git is a **free**, **open-source** **version control system** used for tracking changes in code.

## 2. Configuring Git
Before using Git, set up your username and email:
```bash
 git config --global user.name "JawadAhmadCS"
 git config --global user.email "mjawadahmad41@gmail.com"
```
To check the configured values:
```bash
 git config --list
```

## 3. Setting Up a Git Repository
### Cloning an Existing Repository (GitHub to Local)
1. Open **VS Code**
2. Create a **new folder**
3. Open **terminal** and run:
   ```bash
   git clone https://github.com/JawadAhmadCS/Git.git
   ```
   This will add the repository folder to the local system.

4. Navigate inside the project folder:
   ```bash
   cd Git
   ```

### Creating a New Local Repository
If you want to create a repository locally and push it to GitHub:
1. Inside **VS Code**, run:
   ```bash
   git init
   ```
   This initializes an empty Git repository.
2. Create a repository on **GitHub** (without README file).
3. Link the local repository to GitHub:
   ```bash
   git remote add origin <repository-link>
   ```
4. Verify the remote connection:
   ```bash
   git remote -v
   ```

## 4. Basic Git Commands
### Checking File Status
```bash
git status  # Displays the status of the working directory
```
#### Git Status Categories:
- **Untracked**: New file that Git doesn’t track yet.
- **Modified**: File has been changed.
- **Staged**: File is ready to be committed.
- **Unmodified**: No changes.

### Adding Files to Staging
```bash
git add .              # Stages all changes
git add README.md      # Stages a specific file
```

### Committing Changes
```bash
git commit -m "Updated README.md"
```
**Commit**: Records changes in the repository.

### Pushing Changes to Remote Repository
```bash
git push origin main  # Uploads local commits to the remote repository
```

### Pushing for the First Time
To avoid specifying the branch every time:
```bash
git push -u origin main
```

## 5. Git Branching
**Branches allow multiple developers to work on different features separately.**

### Checking Available Branches
```bash
git branch
```
### Creating a New Branch
```bash
git checkout -b feature2  # Creates and switches to a new branch
```
### Switching Between Branches
```bash
git checkout feature1
```
### Renaming a Branch
```bash
git branch -M main
```
### Deleting a Branch
```bash
git branch -d feature1
```

## 6. Merging and Pull Requests
### Merging Branches Locally
```bash
git merge main  # Merges the 'main' branch into the current branch
```
### Creating a Pull Request on GitHub
1. Go to **GitHub repository**.
2. Select the feature branch.
3. Click **Compare & Pull Request**.
4. Review the changes and click **Merge**.

## 7. Syncing Local and Remote Repositories
### Pulling Changes from Remote to Local
```bash
git pull origin main
```
This fetches and updates the local repository.

## 8. Viewing and Resetting Commits
### Viewing Commit History
```bash
git log  # Shows commit history
```
### Resetting Commits
#### Reset a specific file
```bash
git reset index.html
```
#### Undo the last commit
```bash
git reset HEAD~1
```
#### Reset to a specific commit
```bash
git reset <commit-hash>
```
#### Reset Hard (removes all changes)
```bash
git reset --hard <commit-hash>
```

## 9. Other Useful Commands
### Clearing Terminal
```bash
clear  # Clears the terminal screen
```
### Listing Files in a Directory
```bash
ls      # Shows all files in the directory
ls -a   # Shows hidden files as well
```
### Comparing Current Branch with Main
```bash
git diff main
```

## 10. Forking a Repository
**Forking**: Copying someone else’s GitHub repository to your account to modify it independently.

---

# README.md

## Git Commands Cheat Sheet

### Setting Up Git
```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

### Creating a Repository
```bash
git init
```

### Cloning a Repository
```bash
git clone <repository-url>
```

### Checking Repository Status
```bash
git status
```

### Adding Files to Staging
```bash
git add .
```

### Committing Changes
```bash
git commit -m "Your commit message"
```

### Pushing Changes to Remote
```bash
git push origin main
```

### Pulling Changes from Remote
```bash
git pull origin main
```

### Creating and Switching Branches
```bash
git checkout -b new-branch
```

### Merging Branches
```bash
git merge main
```

### Deleting a Branch
```bash
git branch -d old-branch
```

### Resetting Commits
```bash
git reset HEAD~1  # Undo last commit
git reset --hard <commit-hash>  # Reset to a specific commit
```

### Viewing Commit History
```bash
git log
```

---

This **README.md** file contains a summary of important Git commands. Save it in your repository for quick reference!
