Here is a **professional, ADVANCED command-line workflow** you can use for **every GitHub task** (README included, clean commits, pull request ready).
This is **industry-standard** and perfect for learning + portfolio + YouTube demos.

---

## 🚀 Complete GitHub Task – Command Line Workflow

### 1️⃣ Clone the repository

```bash
git clone https://github.com/USERNAME/REPOSITORY-NAME.git
cd REPOSITORY-NAME
```

---

### 2️⃣ Create a new feature branch

```bash
git checkout -b feature/task-name
```

---

### 3️⃣ Create / update README.md

```bash
touch README.md
```

(Optional – open in editor)

```bash
code README.md
```

---

### 4️⃣ Check file status

```bash
git status
```

---

### 5️⃣ Add all changes

```bash
git add .
```

*or add only README*

```bash
git add README.md
```

---

### 6️⃣ Commit with a professional message

```bash
git commit -m "docs: add detailed README for task"
```

---

### 7️⃣ Push the branch to GitHub

```bash
git push origin feature/task-name
```

---

### 8️⃣ Create Pull Request (CLI way – Advanced)

If **GitHub CLI** is installed:

```bash
gh pr create --base main --head feature/task-name --title "Add task README" --body "Added advanced README with proper documentation"
```

---

## 🔥 Extra Professional Commands (Recommended)

### Set upstream branch

```bash
git push -u origin feature/task-name
```

---

### View commit history

```bash
git log --oneline
```

---

### Sync with main branch

```bash
git checkout main
git pull origin main
git checkout feature/task-name
git merge main
```

---

### Delete branch after merge

```bash
git branch -d feature/task-name
git push origin --delete feature/task-name
```

---

## 🧠 Professional Commit Message Examples

```bash
feat: add pull request demo
docs: update README with task details
fix: correct git workflow steps
refactor: improve project structure
```

---

## ✅ This Workflow Shows You Are:

✔ Industry-ready
✔ Open-source friendly
✔ Professional developer
✔ Serious about documentation

---

If you want next:

* 🔥 **One-line commands cheat sheet**
* 📘 **Git commands for beginners → advanced**
* 🎥 **Explain these commands in simple English (for YouTube)**
* 🧩 **GitHub task automation script**

Just tell me 💻🚀


I think you mean **Git branches** (not *brand*).
Here are **ALL the command-line ways to check branches** — from beginner to **advanced level** ✅

---

## 🔍 Check ALL Git Branches (Command Line)

### 1️⃣ Check **local branches**

```bash
git branch
```

👉 Shows branches on your computer
👉 `*` indicates the current branch

---

### 2️⃣ Check **remote branches**

```bash
git branch -r
```

👉 Shows branches on GitHub (origin)

---

### 3️⃣ Check **ALL branches (local + remote)** ⭐

```bash
git branch -a
```

Example output:

```text
* main
  feature/readme-task
  remotes/origin/main
  remotes/origin/feature/readme-task
```

---

## 🧠 Advanced Branch Checking

### 4️⃣ Show branch with last commit

```bash
git branch -v
```

---

### 5️⃣ Show merged branches

```bash
git branch --merged
```

---

### 6️⃣ Show branches NOT merged

```bash
git branch --no-merged
```

---

### 7️⃣ Show current branch only

```bash
git branch --show-current
```

---

## 🌐 Check branches directly from remote (advanced)

```bash
git ls-remote --heads origin
```

---

## 🚀 Professional Workflow Tip

Before creating a new branch:

```bash
git fetch
git branch -a
```

This ensures you are working with the **latest branch list**.

---

## ✅ Quick Cheat Sheet (Save This)

```bash
git branch        # local
git branch -r     # remote
git branch -a     # all
```

---

If you want next:

* 🔥 **How to switch branches safely**
* 🧠 **Branch naming best practices**
* 🎥 **Explain branches in simple English (for YouTube)**
* 🧩 **Git branch workflow (company standard)**

Just tell me 👍
