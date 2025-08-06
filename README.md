##Start Here Bro
### 🚀 Your Personalized Kickstart Reference 

#### 📁 1. Git + GitHub

```bash
# Setup
git init
git remote add origin <url>
git branch -M main

# Daily
git status
git add .
git commit -m "..."
git push origin main

# Clone + Branch
git clone <repo>
git checkout -b feature-x

# Pull changes
git pull origin main
```

---

#### ⚛️ React (Vite)

```bash
npm create vite@latest my-app --template react
cd my-app
npm install
npm run dev
```

#### ✅ Checklist

* [ ] Install Tailwind `npm install -D tailwindcss postcss autoprefixer`
* [ ] Setup `tailwind.config.js` and `index.css`
* [ ] Add `.env` for API keys or URLs
* [ ] Basic `useState` / `useEffect` test

---

#### 🧡 Svelte + Tailwind

```bash
npm create svelte@latest my-app
cd my-app
npm install
npm run dev
```

Tailwind setup:

```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init tailwind.config.cjs -p
```

---

#### 🐍 Flask + Python

```bash
# Virtual env
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install & run
pip install flask
export FLASK_APP=app.py
flask run
```

---

#### 🌿 Django

```bash
pip install django
django-admin startproject mysite
cd mysite
python manage.py runserver
```

---

#### 🐳 Docker (Basic)

```bash
docker build -t myapp .
docker run -p 5000:5000 myapp

# Compose
docker-compose up
docker ps
```

---

#### 🧠 SQLite & MySQL

```bash
# SQLite (Python)
import sqlite3
conn = sqlite3.connect('db.sqlite3')

# MySQL CLI
mysql -u root -p
SHOW DATABASES;
USE your_db;
```

---

#### More Git
```bash
# Create a new local Git repository
git init  # Start version control in current folder

# Set your user info (done once per machine or repo)
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

---

### 🌐 REMOTE SETUP (GitHub etc.)

```bash
# Link to a remote repository (GitHub, GitLab, etc.)
git remote add origin https://github.com/yourname/repo.git

# Set default branch to main (recommended)
git branch -M main

# Push first commit to remote
git push -u origin main  # "-u" sets upstream so future push is just "git push"
```

---

### 🛠️ COMMON WORKFLOW COMMANDS

```bash
# Check current status (what’s changed, staged, untracked, etc.)
git status

# See changes made to files (before staging)
git diff

# Stage all changes
git add .

# OR stage a specific file
git add file.py

# Commit changes with message
git commit -m "Add login form with validation"

# Push changes to GitHub
git push

# Pull the latest changes from remote
git pull
```

---

### 🌳 BRANCHING & MERGING

```bash
# Create and switch to a new branch
git checkout -b feature/login-page

# Switch to an existing branch
git checkout main

# Merge a branch into current one
git merge feature/login-page

# Delete a branch (locally)
git branch -d feature/login-page
```

---

### 🔍 LOGS & HISTORY

```bash
# View commit history
git log

# Compact log (one line per commit)
git log --oneline --graph --all

# Show changes in a specific commit
git show <commit-id>
```

---

### 🧼 CLEANUP & FIXES

```bash
# Unstage a file (undo git add)
git reset HEAD file.js

# Discard all local changes (dangerous!)
git checkout -- .

# Remove untracked files (clean workspace)
git clean -fd
```

---

### 💾 STASHING (SAVE TEMP WORK)

```bash
# Save your uncommitted changes
git stash

# Apply stashed changes back
git stash apply

# View stash list
git stash list
```

---

### ⏪ REVERT & RESET

```bash
# Undo the last commit (keep changes staged)
git reset --soft HEAD~1

# Undo last commit AND unstage changes
git reset --mixed HEAD~1

# Undo last commit AND delete changes
git reset --hard HEAD~1

# Revert a specific commit (creates a new commit)
git revert <commit-id>
```

---

### 🧪 CLONE & CONTRIBUTE

```bash
# Clone a remote repo
git clone https://github.com/user/repo.git

# Fork and work on a project
git checkout -b fix/navbar-bug
git commit -m "Fix mobile navbar collapse"
git push origin fix/navbar-bug
```

---

### 📌 TAGGING

```bash
# Create a new tag (useful for versioning)
git tag v1.0

# Push tags to remote
git push origin --tags
```

---

### 🧭 GIT ALIASES (OPTIONAL BUT USEFUL)

```bash
# Add shortcuts to your git commands
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.cm 'commit -m'
git config --global alias.st status
```

Then you can run:

```bash
git co main      # instead of checkout
git cm "message" # instead of commit -m
```

---

### 🧠 RECOMMENDED DAILY WORKFLOW

```bash
git status         # See what’s going on
git pull origin main
git checkout -b new-feature
# Make changes...
git add .
git commit -m "Implement new feature"
git push origin new-feature
```

---

## 🟢 **Git Kickstart Advanced Commands**

```bash
# 1️⃣ STASH: Save uncommitted changes (clean working directory)
git stash save "WIP: My changes"

# See list of stashes
git stash list

# Re-apply most recent stash
git stash apply

# Apply and remove stash
git stash pop

# 2️⃣ CHERRY-PICK: Apply a specific commit to your current branch
# (Example: commit hash = abc123)
git cherry-pick abc123

# 3️⃣ REBASE: Replay your commits onto another base branch
# (Example: rebase current branch onto 'main')
git fetch origin
git rebase origin/main

# Abort rebase if conflicts are too messy
git rebase --abort

# Continue rebase after resolving conflicts
git rebase --continue

# 4️⃣ RESET: Move HEAD and optionally working directory
# --soft keeps changes staged
git reset --soft HEAD~1

# --mixed keeps changes unstaged (default)
git reset --mixed HEAD~1

# --hard discards changes permanently
git reset --hard HEAD~1

# 5️⃣ FETCH: Get latest commits from remote WITHOUT merging
git fetch origin

# See what changed compared to your branch
git log HEAD..origin/main --oneline

# Merge fetched changes manually
git merge origin/main
```

---

### ⚡ **Quick Tips**

✅ `stash` = Hide your local changes temporarily
✅ `cherry-pick` = Grab *one commit* from anywhere
✅ `rebase` = Replay commits as if you branched later (linear history)
✅ `reset` = Move branch pointer, optionally discard work
✅ `fetch` = Sync remote refs without changing your files

---

