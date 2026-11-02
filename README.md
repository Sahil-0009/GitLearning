
# Git & GitHub – Lesson 1

## 1. What is Git?
Git is a Distributed Version Control System (DVCS) used to track code changes, manage project versions, and collaborate with developers.

## 2. Git vs GitHub
- **Git:** Tracks changes in source code.
- **GitHub:** Online platform to host and share Git repositories.

## 3. Important Git Concepts
- **Repository:** Project tracked by Git.
- **Commit:** Saved snapshot of changes.
- **Branch:** Separate line of development.
- **Staging Area:** Prepares changes for commit.
- **Remote:** Online repository.
- **Push:** Upload commits to GitHub.
- **Pull:** Download and integrate remote changes.
- **Clone:** Copy an existing repository.

## 4. Git Workflow

`Working Directory → Staging Area → Local Repository → Remote Repository`

- `git add` – Stage changes.
- `git commit` – Save changes locally.
- `git push` – Upload commits to GitHub.

## 5. Git Installation & Configuration

Download: https://git-scm.com/install/windows

```bash
git --version

git config --global user.name "Your Name"
git config --global user.email "your@email.com"

git config --list
```

## 6. Important Git Commands

| Command | Description |
|---|---|
| `git init` | Initialize repository |
| `git status` | Check file status |
| `git add .` | Stage all changes |
| `git commit -m "message"` | Save changes |
| `git log` | View commit history |
| `git diff` | View unstaged changes |
| `git clone URL` | Clone repository |
| `git push` | Upload commits |
| `git pull` | Retrieve and integrate changes |
| `git branch` | View branches |

## 7. Connect Git with GitHub

```bash
git init
git add .
git commit -m "Initial commit"

git branch -M main
git remote add origin YOUR_REPOSITORY_URL

git push -u origin main
```

## 8. What is .gitignore?

`.gitignore` tells Git which untracked files and folders to ignore.

Example:

```gitignore
*.class
target/
.idea/
.env
*.log
```

**Never upload passwords, API keys, or sensitive credentials.**

## 9. Important Differences

| Git Command | Purpose |
|---|---|
| `git add` | Stage changes |
| `git commit` | Save changes locally |
| `git push` | Upload commits |
| `git pull` | Download and integrate changes |
| `git init` | Create a new local repository |
| `git clone` | Copy an existing repository |

## Key Takeaway

**Remember the basic Git workflow:**

`Edit → Add → Commit → Push`

Git helps developers track changes, maintain project history, and collaborate efficiently.