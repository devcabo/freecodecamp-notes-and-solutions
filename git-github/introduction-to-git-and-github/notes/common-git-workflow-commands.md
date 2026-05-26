# Common Git Workflow Commands

## `git status`

### Purpose

Displays the current state of the repository.

### What It Shows

- modified files
- staged files
- untracked files
- current branch information

### Command

```bash
git status
```

### Practical Example

```text
On branch main

Changes not staged for commit:
  modified: README.md

Untracked files:
  notes/git-workflow.md
```

This command is commonly used before creating commits.

---

# `git diff`

### Purpose

Displays the exact changes made inside tracked files.

### What It Shows

- added lines
- removed lines
- modified content

### Command

```bash
git diff
```

### Practical Example

```text
- Git is a version control system.
+ Git is a distributed version control system.
```

This command helps developers review modifications before committing changes.

---

# `git add`

### Purpose

Stages files to be included in the next commit.

### Command

```bash
git add <file-name>
```

Stage a specific file:

```bash
git add README.md
```

Stage all modified files:

```bash
git add .
```

### Practical Example

```bash
git add .
```

This command stages all modified and new files in the current directory.

---

# `git commit`

### Purpose

Creates a snapshot of the staged changes in the repository.

### Command

```bash
git commit -m "commit message"
```

### Practical Example

```bash
git commit -m "docs: update Git workflow notes"
```

This command creates a commit containing the staged changes and associates it with a descriptive message.

---

# `git push`

### Purpose

Uploads local commits to a remote repository such as GitHub.

### Command

```bash
git push origin main
```

### Practical Example

```bash
git push origin main
```

In this example:
- `origin` refers to the remote repository
- `main` refers to the branch being uploaded

This command synchronizes local commits with GitHub.

---

# `git pull`

### Purpose

Downloads and integrates the latest changes from a remote repository into the local repository.

### Command

```bash
git pull
```

### Practical Example

```text
Developer A pushes new commits to GitHub.

Developer B runs `git pull` to update the local repository before continuing development.
```

This helps keep local projects synchronized with remote repositories.

---

# `git clone`

### Purpose

Creates a local copy of a remote repository.

### Command

```bash
git clone <repository-url>
```

### Practical Example

```bash
git clone https://github.com/user/project.git
```

After running the command, Git downloads the entire repository, including:
- project files
- commit history
- branches

---

# `git log`

### Purpose

Displays the commit history of the repository.

### Command

```bash
git log
```

### Practical Example

```text
commit a1b2c3d4
Author: USER
Date: Mon May 26

    docs: update Git workflow notes
```

This command helps developers review previous commits and project history.

---

# `git log --oneline`

### Purpose

Displays a simplified version of the commit history.

### Command

```bash
git log --oneline
```

### Practical Example

```text
a1b2c3d docs: update Git workflow notes
e5f6g7h feat: add repository structure
```

This format is useful for quickly navigating commit history.

---

# `git show`

### Purpose

Displays detailed information about a specific commit.

### Command

```bash
git show <commit-id>
```

### Practical Example

```bash
git show a1b2c3d
```

This command displays:
- commit information
- author information
- changed files
- added and removed lines

---

# Common Daily Git Workflow

### Example Workflow

```bash
git status
git add .
git commit -m "docs: update Git notes"
git push origin main
```

### Workflow Explanation

1. Check repository changes
2. Stage modified files
3. Create a commit
4. Upload changes to GitHub