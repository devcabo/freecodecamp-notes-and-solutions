# Daily Git Workflow After Linking the Repository

## Overview

After connecting your local repository to GitHub for the first time, the workflow becomes much simpler.

This note explains the standard Git workflow used to save changes, create commits and upload updates to GitHub.

---

# Step 1 - Check Repository Status

Before creating a commit, verify the current repository state:

```bash
git status
```

This command shows:
- modified files
- deleted files
- new files
- staged and unstaged changes

---

# Step 2 - Add Changes to the Staging Area

To add all modified files:

```bash
git add .
```

You can also add specific files:

```bash
git add README.md
```

The staging area prepares files for the next commit.

---

# Step 3 - Create a Commit

Create a commit with a clear and descriptive message:

```bash
git commit -m "docs: add Git branch explanations"
```

A commit creates a snapshot of the project at a specific moment.

Good commit messages help organize project history and make collaboration easier.

---

# Step 4 - Upload Changes to GitHub

Send the commit to the remote repository:

```bash
git push
```

Git uploads the local commits to GitHub.

---

# Complete Daily Workflow

The standard workflow is:

```bash
git status
git add .
git commit -m "your commit message"
git push
```

---

# Example Workflow

```bash
git status
git add .
git commit -m "docs: add branch workflow notes"
git push
```

---

# Common Commit Prefixes

## docs:
Used for documentation and notes.

Example:

```bash
git commit -m "docs: add SQL JOIN explanations"
```

---

## feat:
Used for new features or code additions.

Example:

```bash
git commit -m "feat: create Bash automation script"
```

---

## fix:
Used for bug fixes or corrections.

Example:

```bash
git commit -m "fix: correct branch example syntax"
```