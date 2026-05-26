## Module Overview

This exercise teaches how to upload a local repository to GitHub by connecting the local project to a remote repository using the repository URL provided by GitHub.

---

## Question 01

What command would you use to initialize a Git repository in an existing local directory?

### Answer

```bash
git init
```

### Explanation

The `git init` command creates a new Git repository inside the current directory.

After initialization, Git starts tracking:
- file changes
- commits
- branches
- project history

This command is commonly used when starting version control for an existing local project.

Git creates a hidden `.git/` directory that stores all repository metadata and version history information.

### Practical Example

```bash
git init
```

Example project structure after initialization:

```text
portfolio-project/
├── README.md
├── src/
└── .git/
```

The `.git/` directory contains all version control data used by Git.

---

## Question 02

What does the `git commit -m` command do?

### Answer

It commits your changes with a short message you provide.

### Explanation

The `git commit -m` command creates a new commit containing the staged changes in the repository.

The `-m` flag allows developers to include a short descriptive commit message directly in the command line.

Commit messages help developers:
- describe changes
- track project history
- understand previous updates
- improve collaboration

Well-written commit messages make repositories easier to maintain and navigate.

### Practical Example

```bash
git commit -m "docs: add GitHub integration notes"
```

This command creates a new commit containing the staged files and associates it with the provided message.

Example workflow:

```bash
git add .
git commit -m "feat: create repository structure"
```

---

## Question 03

Which of the following commands is used to push up changes to remote repository?

### Answer

```bash
git push
```

### Explanation

The `git push` command uploads local commits from a local repository to a remote repository such as GitHub.

This command is commonly used to:
- publish changes
- synchronize repositories
- share updates with other developers
- back up project history remotely

Before using `git push`, the repository usually needs to:
- be connected to a remote repository
- contain at least one commit

### Practical Example

```bash
git push origin main
```

In this example:
- `origin` refers to the remote repository
- `main` refers to the branch being uploaded

Example workflow:

```bash
git add .
git commit -m "docs: update repository documentation"
git push origin main
```

This sequence stages files, creates a commit and uploads the changes to GitHub.