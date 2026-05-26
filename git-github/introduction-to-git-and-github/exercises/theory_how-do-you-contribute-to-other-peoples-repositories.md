## Module Overview

This module focuses on collaborative development and explains how developers can contribute to other repositories by creating commits and proposing changes.

Before contributing directly to a project, developers usually need permission to access the original repository. If direct access is not available, the recommended workflow is to create a fork of the repository.

A fork creates a personal copy of the original project under your own GitHub account. This allows developers to:
- experiment safely
- make changes independently
- create new features
- fix bugs
- propose improvements without affecting the original project

After making changes locally, contributors can submit a pull request so project maintainers can review and potentially merge the proposed updates into the main repository.

The module also introduces common collaboration workflows used in open-source and team-based development environments.

---

## Question 01

Why do you need to fork a repository when contributing to someone else's project?

### Answer

Because you generally don't have write access to someone else's repository.

### Explanation

Most public repositories on GitHub do not allow external developers to push changes directly to the original project.

Forking creates a personal copy of the repository under your own GitHub account, allowing you to:
- make changes safely
- experiment independently
- create commits without affecting the original project

This workflow is commonly used in open-source development because it allows maintainers to review proposed changes before merging them into the main repository.

Forking also helps maintain project stability and security by preventing unauthorized modifications.

### Practical Example

```text
A developer wants to fix a typo in an open-source project's documentation.

Since the developer does not have direct write access to the original repository, they first create a fork of the project on GitHub.
```

The developer can then clone the fork locally, make changes and submit a pull request to propose the update.

---

## Question 02

After forking and cloning a repository, what command would you use to add the original repository as a remote?

### Answer

```bash
git remote add upstream [URL]
```

### Explanation

After cloning a forked repository, developers often add the original repository as a second remote called `upstream`.

This allows developers to:
- synchronize their fork with the original project
- download new updates from the main repository
- keep their local copy up to date

In most fork workflows:
- `origin` refers to the developer's personal fork
- `upstream` refers to the original repository

Using an upstream remote is a common practice in collaborative and open-source development.

### Practical Example

```bash
git remote add upstream https://github.com/original/project.git
```

This command connects the local repository to the original project repository.

Developers can then fetch updates from the original repository using:

```bash
git fetch upstream
```

---

## Question 03

What is the conventional name for the remote that points to the original repository you forked from?

### Answer

`upstream`

### Explanation

In Git workflows involving forks, the original repository is commonly referenced using the remote name `upstream`.

This naming convention helps developers distinguish between:
- their personal fork (`origin`)
- the original repository (`upstream`)

Using clear remote names improves repository organization and makes collaborative workflows easier to understand.

Developers frequently use the upstream remote to:
- fetch updates
- synchronize forks
- keep local repositories current with the original project

### Practical Example

```bash
git remote -v
```

Example output:

```text
origin    https://github.com/user/project.git
upstream  https://github.com/original/project.git
```

In this example:
- `origin` points to the developer's fork
- `upstream` points to the original repository