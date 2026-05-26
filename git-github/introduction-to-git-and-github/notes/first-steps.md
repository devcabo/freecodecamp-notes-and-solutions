# Git Installation and Basic Workflow

## Overview

This note explains how to install Git on Windows, configure it correctly and use the basic workflow to manage and upload projects to GitHub.

---

# Step 1 - Install Git

Download Git from the official website:

https://git-scm.com/download/win

During the installation, choose the option:

```text
Git from the command line and also from 3rd-party software
```

This option adds Git to the system PATH, allowing it to work directly in the terminal.

---

# Step 2 - Verify Installation

After installing Git, restart the terminal and run:

```bash
git --version
```

Example output:

```text
git version 2.49.0
```

This confirms that Git was installed correctly.

---

# Step 3 - Configure Git Identity

Git needs your username and email to identify commits.

Configure them using:

```bash
git config --global user.name "your-username"
```

```bash
git config --global user.email "your-email@example.com"
```

Example:

```bash
git config --global user.name "devcabo"
git config --global user.email "your-email@example.com"
```

---

# Step 4 - Initialize a Repository

Navigate to your project folder:

```bash
cd C:\freecodecamp-notes-and-solutions
```

Initialize Git:

```bash
git init
```

This creates a local Git repository.

---

# Step 5 - Connect to GitHub

Connect the local repository to the remote GitHub repository:

```bash
git remote add origin https://github.com/devcabo/freecodecamp-notes-and-solutions.git
```

You can verify the connection using:

```bash
git remote -v
```

---

# Step 6 - Add Files

Check repository status:

```bash
git status
```

Add all files to the staging area:

```bash
git add .
```

---

# Step 7 - Create a Commit

Create a commit with a descriptive message:

```bash
git commit -m "docs: add initial Git and GitHub notes"
```

A commit stores a snapshot of the current project state.

---

# Step 8 - Rename Main Branch

Rename the default branch to `main`:

```bash
git branch -M main
```

---

# Step 9 - Push to GitHub

Upload the repository to GitHub:

```bash
git push -u origin main
```

After the first push, future uploads only require:

```bash
git push
```

---

# Daily Git Workflow

The most common Git workflow is:

```bash
git status
git add .
git commit -m "your commit message"
git push
```
