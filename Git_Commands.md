"""# 🛠️ Git & GitHub Command Cheatsheet
> **Quick Reference Guide** for essential Git and GitHub commands. Keep this handy during your development workflows!

---

## ⚙️ Setup & Configuration
Configure your user details, identity, and verify environment settings.

| Command | Description |
| :--- | :--- |
| `git config --global user.name "Name"` | Set your commit author name globally |
| `git config --global user.email "email"` | Set your commit email address globally |
| `git config --list` | View all active configurations and settings |

---

## 📥 Basic Commands
The fundamental commands for tracking and managing local project versions.

| Command | Description |
| :--- | :--- |
| `git init` | Initialize a brand-new local Git repository |
| `git status` | Check the current state of files (tracked, untracked, or modified) |
| `git add <filename>` | Stage a specific file for the next commit |
| `git add .` | Stage **all** modified, deleted, and new files |
| `git commit -m "message"` | Commit staged changes with a descriptive snapshot message |
| `git log` | View the full commit history |
| `git log --oneline` | View a compact, highly scannable one-line-per-commit history |
| `git diff` | Show file modifications that haven't been staged yet |

---

## 🔄 Undoing Changes
Safely back out of mistakes, unstage files, or revert code to a previous state.

| Command | Description |
| :--- | :--- |
| `git restore --staged <file>` | Unstage a file while keeping its local modifications |
| `git restore <file>` | Discard uncommitted changes in a file (**cannot be undone**) |
| `git reset HEAD~1` | Undo the last commit, leaving changes unstaged in your working directory |
| `git reset --hard HEAD~1` | **Destructive:** Undo the last commit and permanently delete all changes |
| `git revert <commit-id>` | Safely create a new commit that completely neutralizes an older commit |

---

## 🌿 Branching
Isolate feature development, experiment safely, and manage parallel code lines.

| Command | Description |
| :--- | :--- |
| `git branch` | List all local branches (your current branch will be highlighted) |
| `git branch <name>` | Create a new branch with the specified name |
| `git checkout <name>` | Switch to an existing branch |
| `git checkout -b <name>` | Create a new branch and immediately switch into it |
| `git merge <branch-name>` | Merge the specified branch's changes into your current active branch |
| `git branch -d <name>` | Delete a local branch safely (checks if changes are merged) |

---

## ☁️ GitHub & Remotes
Collaborate with others by syncing your local repository with cloud hosts.

| Command | Description |
| :--- | :--- |
| `git clone <url>` | Download a full copy of an existing remote repository from GitHub |
| `git remote add origin <url>` | Map your local repository to a remote GitHub repository URL |
| `git remote -v` | View all configured remote repository connections |
| `git push -u origin main` | Push your code to the remote server and link branches for the first time |
| `git push` | Push subsequent local commits upstream to the active remote branch |
| `git pull` | Fetch the latest changes from GitHub and automatically merge them |
| `git fetch` | Download latest changes from GitHub **without** merging them into your code |

---

## 🚀 Advanced Commands
Power-user tools for keeping clean histories and fluid development states.

| Command | Description |
| :--- | :--- |
| `git stash` | Temporarily save uncommitted changes to a clean slate, hiding them away |
| `git stash pop` | Reapply and remove the most recently stashed changes |
| `git stash list` | View all stashed collections of changes waiting to be restored |
| `git rebase main` | Reapply your branch's commits directly on top of the latest `main` branch |

---

## 🔄 Typical Workflow
Follow this standard step-by-step cycle for everyday feature development:

Code output
File successfully generated.

```bash
git pull                       # 1. Pull down the latest code from GitHub
git checkout -b feature        # 2. Create and switch to your new feature branch

# ... make your code modifications ...

git add .                      # 3. Stage your modified work
git commit -m "Your message"   # 4. Commit your changes locally
git push -u origin feature    # 5. Push your feature branch up to GitHub

# ... Open your browser, go to GitHub, and create a Pull Request (PR) ...
# ... Review, approve, and merge the PR into your main branch ...

git checkout main              # 6. Switch back to your local main branch
git pull                       # 7. Grab the freshly merged code from GitHub
git branch -d feature          # 8. Clean up and delete your old local branch

🎉 Congratulations!
You have successfully completed the Git and GitHub guide! You are now equipped to:

[x] Track changes smoothly with Git

[x] Structure and manage collaborative code using branches

[x] Collaborate effortlessly using GitHub remote commands

[x] Confidently navigate and resolve merge conflicts

[x] Leverage advanced productivity workflows like stash and rebase

💡 Pro-Tip: The single best way to master Git is through daily, hands-on practice. Start tracking your school projects, side hustles, or scripts with Git today!
"""