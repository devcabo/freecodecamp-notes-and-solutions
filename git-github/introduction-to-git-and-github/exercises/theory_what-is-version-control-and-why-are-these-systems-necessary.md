## Module Overview

This module explains how Git is a key component of every developer's workflow.

Git is a version control system that helps developers manage changes, track project history and organize code efficiently.

It simplifies collaboration, allows safer experimentation and makes it easier to maintain and recover projects over time.

## Question 01

What is a commit in Git?

### Answer

A snapshot of a specific state of your codebase.

### Explanation

A commit works like a saved snapshot of your project at a specific moment.

It allows developers to track changes over time and easily access previous versions of the project when needed.

Commits are an essential part of version control because they help organize the development history and make collaboration safer and more efficient.

### Practical Example

```bash
git commit -m "initial project setup"
```

## Question 02

Why are branches useful in version control systems like Git?

### Answer

They allow you to work on features in isolation.

### Explanation

A branch is an independent version of the main project that allows developers to work on new features, fixes or experiments without affecting the original codebase.

Branches make development safer by isolating changes until they are ready to be merged into the main project.

### Practical Example

```bash
git checkout -b initial-project-setup
```

## Question 03

Which of the following is NOT mentioned as a version control system in the lesson?

### Answer

Docker

### Explanation

Git is a version control system. It tracks changes made to your source code files over time. It helps teams collaborate on the same codebase without overwriting each other's work and allows you to revert to older versions of your project.

Docker is a containerization platform. It packages your application code along with all its dependencies, libraries, and configuration files into an isolated unit called a "container." This ensures the software runs identically on any computer, eliminating the "it works on my machine" problem.

### Practical Example

```text
A development team uses Git to track changes made to a web application.

Each developer works on separate features and uploads commits to the shared repository without overwriting other team members' work.
```

Example using Git:

```bash
git commit -m "feat: add login page"
```

In contrast, Docker would be used to package and run the application consistently across different environments, not to track source code changes.