# Git Notes

## 1. Introduction to Git
Git is a **free**, **open-source** **version control system** used for tracking changes in code.

## 2. Configuring Git
Before using Git, set up your username and email on git-bash:
```bash
 git config --global user.name "JawadAhmadCS"
```
```bash
 git config --global user.email "youremail@gmail.com"
```
To check the configured values:
```bash
 git config --list
```

## 3. Setting Up a Git Repository
### Cloning an Existing Repository (GitHub to Local)
1. Open **VS Code**
2. Create a **new folder**
3. **Copy link** of repositry from github
4. Open **terminal** and run:
   ```bash
   git clone <repository-url>
   ```
   This will add the repository folder to the local system.

5. Navigate inside the project folder:
   ```bash
   cd Git
   ```

### Creating a New Local Repository
If you want to create a repository locally and push it to GitHub:
1. Inside **VS Code**, create repositry run:
   ```bash
   git init
   ```
   This initializes an Git repository.
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
Displays the status of the working directory
```bash
git status  
```
#### Git Status Categories:
- **Untracked**: New file that Git doesn’t track yet.
- **Modified**: File has been changed.
- **Staged**: File is ready to be committed.
- **Unmodified**: No changes.

### Adding Files to Staging
Stages all changes
```bash
git add .              
```

Stages a specific file
```bash
git add README.md      
```

### Committing Changes
```bash
git commit -m "your message like:Updated README.md"
```
**Commit**: Records changes in the repository.

### Pushing Changes to Remote Repository
Uploads local commits to the remote repository
```bash
git push origin main  
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
Creates and switches to a new branch
```bash
git checkout -b branchname  
```
### Switching Between Branches
```bash
git checkout branchname
```
### Renaming a Branch
```bash
git branch -M branchname
```
### Deleting a Branch
```bash
git branch -d branchname
```

## 6. Merging and Pull Requests
### Merging Branches Locally
Merges the 'main' branch into the current branch
```bash
git merge main  
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
Shows commit history
```bash
git log  
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
this will come by  `git log` history like `git reset 8ff56fa491010809508f1ee147b7d38387035ee6`
#### Reset Hard (removes all changes)
```bash
git reset --hard <commit-hash>
```
## 9. Pull Latest Changes from Upstream  

First, switch to the main branch:  

```bash  
git checkout main  
```  

Then, fetch the latest updates from upstream:  

```bash  
git fetch upstream  
```  

Merge the upstream main branch updates:  

```bash  
git merge upstream/main  
```  

If there are any conflicts, resolve them manually and then:  

```bash  
git add .  
git commit -m "Merged upstream changes"  
```  

## 10. Other Useful Commands
### Clearing Terminal
Clears the terminal screen
```bash
clear  
```
### Listing Files in a Directory
Shows all files in the directory
```bash
ls      
```
Shows hidden files as well
```bash
ls -a   
```
### Comparing Current Branch with Main
```bash
git diff main
```

## 11. Forking a Repository
**Forking**: Copying someone else’s GitHub repository to your account to modify it independently.

---

# Git Commands Cheat Sheet

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

```bash  
git checkout main  
```  

```bash  
git fetch upstream  
```   

```bash  
git merge upstream/main  
```   

```bash  
git add .  
git commit -m "Merged upstream changes"  
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
 Undo last commit
```bash
git reset HEAD~1 
```
Reset to a specific commit
```bash
git reset --hard <commit-hash>  
```

### Viewing Commit History
```bash
git log
```

---

For more [see](https://youtu.be/Ez8F0nW6S-w?si=OXPF4o0uX75L0PQG)

This **README.md** file contains a summary of important Git commands.

