## Module Overview

A branch is an independent line of development inside a Git repository.

It allows developers to work on features, fixes or experiments separately without affecting the main project.

---

## Question 01

What does creating a new branch in Git allow you to do?

### Answer

Make changes without affecting the main branch.

### Explanation

Branches allow developers to work on different parts of a project independently.

By creating a separate branch, developers can:
- test new features
- fix bugs
- experiment safely
- work collaboratively

Changes made inside a branch do not affect the main branch until they are merged.

This helps keep the main project stable while development continues in isolated workspaces.

### Practical Example

```bash
git checkout -b feature/login-page
```

This command:
- creates a new branch called `feature/login-page`
- switches to the new branch immediately

Developers can then work on the new feature without modifying the `main` branch.

---

## Question 02

What does the `*` symbol next to a branch name in `git branch` output indicate?

### Answer

The branch is currently "checked out".

### Explanation

The `git branch` command displays all local branches in the repository.

The `*` symbol indicates the currently active branch, meaning:
- it is the current working branch
- new commits will be created on this branch
- file changes affect this branch

This helps developers identify which branch they are currently working on.

### Practical Example

```bash
git branch
```

Example output:

```text
* main
  feature/navbar
  fix/login-bug
```

In this example:
- `main` is the active branch
- the other branches exist locally but are not currently checked out

---

## Question 03

![Git Branches](../../../assets/images/git-branches.png)

### Answer

Pushes the feature branch and sets it to track the remote branch.

### Explanation

The `git push -u origin <branch-name>` command uploads a local branch to a remote repository and establishes a tracking relationship between the local and remote branches.

The `-u` flag means `--set-upstream`.

After setting the upstream branch:
- future pushes can use only `git push`
- future pulls can use only `git pull`
- Git automatically knows which remote branch is associated with the local branch

This workflow is commonly used when pushing a branch to GitHub for the first time.

### Practical Example

```bash
git push -u origin feature/navbar
```

In this example:
- `origin` refers to the remote repository
- `feature/navbar` is the branch being uploaded

After the first push, the branch becomes linked to the remote branch on GitHub.