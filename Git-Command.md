# **Professional Git Commands** 

## …or create a new repository on the command line

    echo "# mmm" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git branch -M main
    git remote add origin https://github.com/vishwa-oshad/repoName.git
    git push -u origin main


##…or push an existing repository from the command line
    
    git remote add origin https://github.com/vishwa-oshad/mmm.git
    git branch -M main
    git push -u origin main






## 🔹 Daily Workflow (Most Used)

```bash
git status
```

👉 Check file changes

```bash
git pull origin main
```

👉 Get latest code from team

```bash
git add .
```

👉 Stage all changes

```bash
git commit -m "Fix login validation and UI spacing"
```

👉 Commit with clear message

```bash
git push origin main
```

👉 Push to remote repo

---

## 🔹 Branching (Professional Team Work)

```bash
git branch
```

👉 Show branches

```bash
git checkout -b feature/login-ui
```

👉 Create + switch to new branch

```bash
git switch main
```

👉 Switch branch (modern way)

```bash
git merge feature/login-ui
```

👉 Merge feature to main

```bash
git branch -d feature/login-ui
```

👉 Delete branch after merge

---

## 🔹 Fixing Mistakes (Very Important)

```bash
git restore file.txt
```

👉 Undo file changes

```bash
git reset HEAD file.txt
```

👉 Unstage file

```bash
git commit --amend
```

👉 Edit last commit message / add files

```bash
git revert <commit-id>
```

👉 Safely undo a commit (used in teams)

---

## 🔹 Professional History Checking

```bash
git log --oneline --graph --all
```

👉 Beautiful commit history

```bash
git diff
```

👉 See code changes

```bash
git blame file.java
```

👉 See who changed each line

---

## 🔹 Remote Repository

```bash
git remote -v
```

👉 Show remote links

```bash
git fetch origin
```

👉 Download changes without merging

```bash
git pull --rebase
```

👉 Clean professional pull (no extra commits)

---

## 🔹 Stash (Save Work Temporarily)

```bash
git stash
```

👉 Save unfinished work

```bash
git stash pop
```

👉 Restore work

---

## 🔥 Pro-Level Commands (Used by Seniors)

```bash
git cherry-pick <commit-id>
```

👉 Pick specific commit to another branch

```bash
git rebase main
```

👉 Clean linear history

```bash
git tag v1.0.0
```

👉 Release version tagging

---

## ✅ Professional Commit Message Style

Bad ❌

`fix bug`

Good ✅

`Fix crash when user submits empty login form`

`Add payment validation for checkout screen`


---

# ✅ Best Practices to Create Git Branches (Professional Way)

## 🎯 1. Use Clear Branch Naming Rules

### ✅ Recommended Format

```
type/short-description
```

### ✅ Examples

| Purpose     | Branch Name              |
| ----------- | ------------------------ |
| New Feature | `feature/login-ui`       |
| Bug Fix     | `bugfix/crash-on-start`  |
| Hot Fix     | `hotfix/payment-failure` |
| Release     | `release/v1.2.0`         |
| Experiment  | `test/new-animation`     |

❌ Bad:

```
newbranch
mywork
test1
```

---

## 🌳 2. Always Create Branch from Correct Base

### For Features & Bugs → from `develop`

```bash
git checkout develop
git pull origin develop
git checkout -b feature/profile-screen
```

### For Hotfix → from `main`

```bash
git checkout main
git pull origin main
git checkout -b hotfix/login-crash
```

---

## ✍️ 3. Keep Branch Small & Focused

✅ Good:

* One feature per branch
* One bug per branch

❌ Bad:

* Login + Chat + Settings in same branch

This makes code review easy 👍

---

## 🔄 4. Sync With Base Branch Frequently

Before pushing:

```bash
git pull --rebase origin develop
```

Why?

* Avoid merge conflicts
* Keep history clean

---

## 📦 5. Commit Frequently (But Meaningful)

Instead of one big commit ❌
Do small steps ✅

```bash
git commit -m "Add login XML layout"
git commit -m "Connect login API"
git commit -m "Show validation errors"
```

---

## 🔍 6. Push & Open Pull Request Early

```bash
git push origin feature/profile-screen
```

Then open PR:

```
feature/profile-screen → develop
```

Benefits:

* Team can review early
* CI can detect errors

---

## 🧹 7. Delete Branch After Merge

Local:

```bash
git branch -d feature/profile-screen
```

Remote:

```bash
git push origin --delete feature/profile-screen
```

Keeps repo clean 🧼

---

## 🔐 8. Protect Important Branches (GitHub Setting)

On GitHub:

* Protect `main`
* Protect `develop`
* Require Pull Request
* Require CI pass

👉 No one can push directly to main

---

## 🧠 Best Strategy: Git Flow (Recommended for Android)

```
main     → production
develop  → testing
feature  → new work
release  → version prep
hotfix   → urgent fix
```

This is what most companies use ✅

---

## 🎯 For Your Android Projects (Personal + YouTube)

Since you:

* Build POS & M-commerce apps
* Upload to GitHub
* Teach on YouTube

I recommend:

```
main
develop
feature/*
```

Simple but professional 💯

---

## ⚡ One-Line Branch Creation (Pro Tip)

```bash
git switch -c feature/payment-ui develop
```

(Create + switch + from develop)

---

If you want, next I can teach you:
🔥 How to resolve merge conflicts safely
🔥 How to write professional commit messages (with examples)
🔥 GitHub Pull Request best practices

Just tell me, Oshad 💪🚀
