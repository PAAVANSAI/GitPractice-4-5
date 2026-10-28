# 📘 Git & GitHub: Complete Hands-On Guide

A comprehensive, beginner-to-advanced hands-on guide and reference for mastering **Git** and **GitHub** using **Git Bash**.

This repository contains an interactive HTML guide (`Git & GitHub_ Complete Hands-On Guide.html`) structured into **19 detailed modules**. Every module follows a practical **Idea → Commands → Try It** format, complete with visual state flow diagrams and real-world workflows.

---

## 🚀 Quick Navigation

- [📖 Modules Covered](#-modules-covered)
- [🖥️ How to View the Guide](#️-how-to-view-the-guide)
- [⚡ Quick Git Cheat Sheet](#-quick-git-cheat-sheet)
- [🔄 Typical Git Workflow](#-typical-git-workflow)
- [📤 Pushing Changes to GitHub](#-pushing-changes-to-github)

---

## 📖 Modules Covered

| Module | Title | Core Concept / Commands |
| :---: | :--- | :--- |
| **01** | **VCS Basics** | Repositories, snapshots, commits, and why version control matters |
| **02** | **SVN vs. Git** | Centralized vs. distributed version control architecture |
| **03** | **Install & Setup** | Installing Git Bash, configuring `user.name` & `user.email` |
| **04** | **GitHub & Remote Repos** | Creating GitHub accounts, creating clean remote repositories |
| **05** | **HTTPS vs. SSH** | Authentication methods, configuring SSH keys & understanding `origin` |
| **06** | **init, add, commit** | The 3 local zones: Working Directory ➔ Staging Area ➔ Local Repo |
| **07** | **Clone** | Cloning existing remote repositories to local PC (`git clone`) |
| **08** | **Push** | Uploading local commits to remote (`git push origin <branch>`) |
| **09** | **Fetch & Pull** | Syncing changes from remote; difference between `fetch` and `pull` |
| **10** | **.gitignore** | Pattern matching, ignoring sensitive files, caches, and build output |
| **11** | **Branches** | Creating, listing, switching, and deleting branches (`git branch`, `switch`) |
| **12** | **Branching Strategies** | Feature branching, Git Flow, Trunk-based development |
| **13** | **Merge & Conflicts** | Fast-forward vs. 3-way merge, identifying and resolving conflict markers |
| **14** | **Stash** | Temporarily shelving uncommitted changes (`git stash`, `pop`, `list`) |
| **15** | **Checkout & HEAD** | Navigating commits, understanding `HEAD`, and fixing detached HEAD |
| **16** | **Reset & Revert** | Undoing mistakes: `--soft`, `--mixed`, `--hard` reset vs. `git revert` |
| **17** | **Rebase** | Linear history, rebasing feature branches, interactive rebase basics |
| **18** | **Cheat Sheet** | High-frequency command quick reference table |
| **19** | **Master Hands-On** | End-to-end practical project putting all concepts together |

---

## 🖥️ How to View the Guide

The interactive guide is bundled in a single self-contained HTML file.

### Option 1: Open Directly in Browser
- Double-click `Git & GitHub_ Complete Hands-On Guide.html`, or
- Right-click the file and select **Open with** ➔ **Google Chrome** / **Microsoft Edge** / **Firefox**.

### Option 2: Serve Locally (Optional)
If you have Python installed, you can start a local lightweight web server:
```bash
python -m http.server 8000
```
Then visit [`http://localhost:8000`](http://localhost:8000) in your browser.

---

## ⚡ Quick Git Cheat Sheet

### 1. Setup & Config
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
git config --global init.defaultBranch main
git config --list
```

### 2. Daily Workflow
```bash
# Check status of working directory & staging area
git status

# Stage specific file or all files
git add <filename>
git add .

# Commit staged changes
git commit -m "Your descriptive commit message"

# View commit history
git log --oneline --graph --decorate
```

### 3. Remote Synchronization
```bash
# Verify configured remote URLs
git remote -v

# Link local repository to GitHub
git remote add origin https://github.com/USERNAME/REPOSITORY.git

# Push changes to GitHub
git push -u origin <branch-name>

# Pull latest changes from GitHub
git pull origin <branch-name>
```

### 4. Branching
```bash
# Create and switch to a new branch
git checkout -b feature/login
# or (modern Git):
git switch -c feature/login

# List all branches
git branch

# Switch back to main
git switch main

# Merge branch into current branch
git merge feature/login
```

### 5. Undoing & Stashing
```bash
# Discard uncommitted changes in working tree
git restore <file>

# Unstage a file without losing edits
git restore --staged <file>

# Temporarily save uncommitted work
git stash
git stash pop
```

---

## 🔄 Typical Git Workflow

```text
[ Working Directory ]
        │
   git add <file>
        ▼
 [ Staging Area ]
        │
   git commit -m "..."
        ▼
[ Local Repository ]
        │
   git push origin <branch>
        ▼
[ GitHub (Remote) ]
```

---

## 📤 Pushing Changes to GitHub

To push this README and your project files to your GitHub repository:

1. **Check status:**
   ```bash
   git status
   ```

2. **Stage the new README file:**
   ```bash
   git add README.md
   ```

3. **Commit the changes:**
   ```bash
   git commit -m "Add comprehensive README guide"
   ```

4. **Push to GitHub:**
   ```bash
   git push origin master
   ```
   *(Note: If your default remote branch is named `main`, use `git push -u origin main`)*

---

## 📄 License & Attribution

Created for learning, hands-on practice, and quick reference for Git and GitHub workflows. Feel free to fork, customize, and share!

