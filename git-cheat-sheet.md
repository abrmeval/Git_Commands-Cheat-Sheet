# 🧾 Git Cheat Sheet

A comprehensive guide with essential Git commands, explanations, and usage examples.

---

## 🔧 Configuration
| Command | Description | Example |
|--------|-------------|---------|
| `git config --global user.name "Your Name"` | Sets your Git username | `git config --global user.name "Alice"` |
| `git config --global user.email "you@example.com"` | Sets your Git email | `git config --global user.email "alice@example.com"` |
| `git config --list` | Lists all Git config values | `git config --list` |

---

## 📂 Repository Basics
| Command | Description | Example |
|--------|-------------|---------|
| `git init` | Initializes a new repo | `git init` |
| `git clone <url>` | Clones a remote repo | `git clone https://github.com/user/repo.git` |
| `git status` | Shows working directory status | `git status` |

---

## 📝 Staging & Committing
| Command | Description | Example |
|--------|-------------|---------|
| `git add <file>` | Stages a file | `git add app.js` |
| `git add .` | Stages all changes | `git add .` |
| `git commit -m "msg"` | Commits staged files | `git commit -m "Initial commit"` |
| `git commit -am "msg"` | Adds & commits tracked files | `git commit -am "Quick fix"` |
| `git commit --amend` | Modifies last commit | `git commit --amend -m "Correct commit message"` |

---

## 🔍 Viewing Changes & History
| Command | Description | Example |
|--------|-------------|---------|
| `git log` | Shows commit history | `git log` |
| `git log --oneline` | Summary format | `git log --oneline` |
| `git diff` | Shows unstaged changes | `git diff` |
| `git diff --staged` | Shows staged changes | `git diff --staged` |
| `git show <commit>` | Shows specific commit details | `git show abc123` |

---

## 🌿 Branching
| Command | Description | Example |
|--------|-------------|---------|
| `git branch` | Lists branches | `git branch` |
| `git branch <name>` | Creates new branch | `git branch feature-nav` |
| `git checkout <branch>` | Switches branches | `git checkout feature-nav` |
| `git checkout -b <name>` | Creates and switches branch | `git checkout -b hotfix-logout` |
| `git branch -d <name>` | Deletes local branch | `git branch -d old-feature` |

---

## 🔁 Merging Branches (Ways to Merge)
| Command | Description | Example |
|--------|-------------|---------|
| `git merge <branch>` | Fast-forward or 3-way merge | `git merge feature` |
| `git merge --no-ff <branch>` | Forces a merge commit | `git merge --no-ff feature` |
| `git merge --squash <branch>` | Combines all commits into one before merging | `git merge --squash feature` |
| `git merge --abort` | Cancels a failed/conflicting merge | `git merge --abort` |

---

## 🔁 Rebasing
| Command | Description | Example |
|--------|-------------|---------|
| `git rebase <branch>` | Replays commits on top of another branch | `git rebase main` |
| `git rebase -i HEAD~n` | Interactive rebase to edit/squash commits | `git rebase -i HEAD~3` |
| `git rebase --continue` | Continues after resolving conflict | `git rebase --continue` |
| `git rebase --abort` | Aborts the rebase | `git rebase --abort` |

---

## 🔄 Renaming Branches
| Command | Description | Example |
|--------|-------------|---------|
| `git branch -m <new>` | Renames current branch | `git branch -m new-name` |
| `git branch -m <old> <new>` | Renames specific branch | `git branch -m old-name new-name` |
| `git push origin :<old>` | Deletes old remote branch | `git push origin :old-name` |
| `git push origin <new>` | Pushes renamed branch to remote | `git push origin new-name` |
| `git push --set-upstream origin <new>` | Sets tracking for renamed branch | `git push --set-upstream origin new-name` |

---

## 📦 Stashing
| Command | Description | Example |
|--------|-------------|---------|
| `git stash` | Stashes current changes | `git stash` |
| `git stash list` | Shows saved stashes | `git stash list` |
| `git stash apply` | Reapplies the latest stash | `git stash apply` |
| `git stash pop` | Applies and removes the latest stash | `git stash pop` |
| `git stash drop` | Deletes a specific stash | `git stash drop stash@{0}` |

---

## ☁️ Remote Repositories
| Command | Description | Example |
|--------|-------------|---------|
| `git remote -v` | Shows remotes | `git remote -v` |
| `git remote add <name> <url>` | Adds a new remote | `git remote add origin https://github.com/user/repo.git` |
| `git remote set-url origin <url>` | Changes a remote URL | `git remote set-url origin https://new.git` |

---

## 🔁 Syncing with Remote
| Command | Description | Example |
|--------|-------------|---------|
| `git fetch` | Gets changes from remote | `git fetch origin` |
| `git pull` | Fetches and merges | `git pull origin main` |
| `git push` | Pushes changes to remote | `git push origin main` |
| `git push -u origin <branch>` | Sets upstream and pushes | `git push -u origin feature-nav` |

---

## 🏷️ Tags
| Command | Description | Example |
|--------|-------------|---------|
| `git tag` | Lists tags | `git tag` |
| `git tag <name>` | Creates a tag | `git tag v1.0` |
| `git push origin <tag>` | Pushes a tag | `git push origin v1.0` |

---

## 🧹 Cleaning Up
| Command | Description | Example |
|--------|-------------|---------|
| `git clean -f` | Removes untracked files | `git clean -f` |
| `git clean -fd` | Removes untracked files and dirs | `git clean -fd` |
