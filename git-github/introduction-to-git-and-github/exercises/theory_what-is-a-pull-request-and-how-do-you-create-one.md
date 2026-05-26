## Module Overview

This module explains pull requests and how they are used on GitHub to propose changes to a repository.

A pull request is a collaborative feature that allows developers to submit their code changes for review before they are merged into the main project.

Instead of directly modifying the original repository, developers can:
- create branches
- fork repositories
- make commits independently
- submit pull requests for review

Pull requests improve collaboration by allowing other developers to:
- review code
- discuss changes
- suggest improvements
- detect bugs
- approve or reject updates before merging

They are one of the most important workflows in modern software development and are widely used in:
- open-source projects
- team-based development
- professional engineering environments

GitHub provides a dedicated interface for managing pull requests, making it easier to track discussions, commits and proposed modifications throughout the review process.

---

## Question 01

What is a pull request in GitHub?

### Answer

A request to pull changes from one branch into another branch.

### Explanation

A pull request is a GitHub feature used to propose changes from one branch to another, usually into the main project branch.

Pull requests allow developers to:
- review code before merging
- discuss modifications
- suggest improvements
- identify bugs
- approve or reject changes

They help teams collaborate safely by preventing unreviewed code from being merged directly into important branches.

Pull requests are commonly used in collaborative and open-source development workflows.

### Practical Example

```text
A developer creates a new feature in a branch called `feature/navbar`.

After finishing the implementation, the developer opens a pull request to merge the branch into `main`.
```

Other team members can then review the code and approve the changes before merging.

---

## Question 02

In a pull request, what do the terms "base" and "compare" (or "head") refer to?

### Answer

"Base" is the target branch; "compare" is the source branch.

### Explanation

When creating a pull request on GitHub:
- the `base` branch is the branch that will receive the changes
- the `compare` or `head` branch contains the proposed changes

GitHub compares the differences between both branches and displays:
- modified files
- commits
- added and removed lines

This helps developers review the proposed updates before merging.

In most workflows:
- `main` is usually the base branch
- feature branches are usually the compare branch

### Practical Example

```text
Base branch: main
Compare branch: feature/login-page
```

In this example:
- changes from `feature/login-page` are being proposed
- the updates would be merged into `main` if approved

---

## Question 03

Which of the following is NOT a merge strategy mentioned when merging a pull request on GitHub?

### Answer

Fork and Merge

### Explanation

GitHub provides different merge strategies for integrating pull requests into a repository.

Common merge strategies include:
- Create a merge commit
- Squash and merge
- Rebase and merge

These strategies define how commits from the pull request are integrated into the target branch.

`Fork and Merge` is not a merge strategy. It is a collaboration workflow where developers contribute to repositories through forks and pull requests.

Understanding merge strategies helps developers maintain:
- cleaner commit history
- organized project structure
- better collaborative workflows

### Practical Example

```text
A pull request contains five commits from a feature branch.

The maintainer chooses "Squash and merge" to combine all commits into a single commit before merging into the main branch.
```

This helps keep the repository history cleaner and easier to read.