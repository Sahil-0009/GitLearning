
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




# Git Lesson 2 – Branching and Merging



## 1. What is Branching?
A branch is an independent line of development that allows developers to work on different features without affecting the main code.

- `main` – Main project branch.
- `feature/login` – Login feature branch.
- `feature/payment` – Payment feature branch.

## 2. Why Use Branches?
- Work on multiple features independently.
- Avoid disturbing main code.
- Fix bugs separately.
- Collaborate with team members.
- Test features before merging.

## 3. Important Branch Commands

| Command | Description |
|---|---|
| `git branch` | View branches |
| `git branch feature/login` | Create a branch |
| `git switch feature/login` | Switch branch |
| `git switch -c feature/login` | Create and switch |
| `git checkout main` | Switch branch (older command) |
| `git checkout -b feature/login` | Create and switch (older command) |
| `git branch -d feature/login` | Delete merged branch |

## 4. What is Git Merge?
Merge combines changes from one branch into another.

```bash
# Switch to destination branch
git switch main

# Merge feature branch
git merge feature/login
```

## 5. Types of Merge

- **Fast-forward Merge:** Moves the branch pointer forward when no separate commits have been made on the destination branch.
- **Three-way Merge:** Combines changes using the common ancestor and the latest commits of both branches.

## 6. What is a Merge Conflict?
A merge conflict occurs when Git cannot automatically combine changes, often because different branches modify the same lines.

**Resolution steps:**
1. Open the conflicted file.
2. Review both changes.
3. Select or manually combine the correct changes.
4. Remove conflict markers.
5. Save the file.
6. Stage and commit the resolved changes.

```bash
git status
git add .
git commit -m "Resolve merge conflict"
```

## 7. Practical Branch Workflow

```bash
# Create and switch branch
git switch -c feature/student

# Stage and commit changes
git add .
git commit -m "Add Student class"

# Switch to main
git switch main

# Merge feature
git merge feature/student

# Upload changes
git push origin main
```

## 8. Delete a Branch

```bash
# Delete local branch
git branch -d feature/student

# Delete remote branch
git push origin --delete feature/student
```

## 9. Git Branching in Companies

Typical industry workflow:

`Create Branch → Write Code → Commit → Push → Pull Request → Code Review → Merge`

- **Pull Request (PR):** A request to review and merge changes into another branch.
- Developers generally work on feature branches instead of directly modifying main.

## 10. Important Interview Questions

1. What is a Git branch?
2. Why do we use branching?
3. Difference between `git branch` and `git switch`?
4. Difference between fast-forward and three-way merge?
5. What is a merge conflict?
6. How do you resolve merge conflicts?
7. Difference between `git branch -d` and `git branch -D`?
8. What is a Pull Request?

## Key Takeaway

- **Branch:** Independent development path.
- **Switch:** Move between branches.
- **Merge:** Combine branch changes.
- **Conflict:** Changes Git cannot automatically combine.
- **Pull Request:** Request code review and merging.

**Remember:**

`Create Branch → Develop → Commit → Merge → Push`