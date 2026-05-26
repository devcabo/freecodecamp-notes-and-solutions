## Module Overview

This module explains what a repository is and describes it as a container used to store and manage project files, source code and version history. Repositories can be local, stored on your own computer, or remote, hosted on platforms such as GitHub.

The module also introduces repository templates, which help developers create new projects more efficiently by providing predefined structures and configuration files.

Its main focus is teaching the integration between Git and GitHub, including how to create repositories, connect them to remote platforms and start pushing changes.

## Question 01

What does a repository primarily function as in Git?

### Answer

A container for a project and its files.

### Explanation

A Git repository is a directory used to store project files, source code and version history.

Repositories help developers:
- organize project files
- track changes over time
- collaborate with other developers
- manage different versions of a project

Repositories can be:
- local, stored on a computer
- remote, hosted on platforms such as GitHub or GitLab

Git uses repositories to maintain the complete history of changes made to a project.

### Practical Example

```text
portfolio-project/
├── README.md
├── src/
├── assets/
└── .git/
```

In this example:
- the project files are stored inside the repository
- the `.git/` folder contains all Git version control information
- developers can track changes and collaborate on the project

---

## Question 02

When creating a repository on GitHub, which of the following is NOT an automatic file generation option?

### Answer

A `package.json` file.

### Explanation

When creating a new repository on GitHub, developers can optionally generate some common files automatically.

These files may include:
- a `README.md` file
- a `.gitignore` file
- an open-source license

These options help developers initialize and organize repositories more quickly.

However, a `package.json` file is not generated automatically by GitHub because it is specific to Node.js projects and is usually created manually or through tools such as `npm init`.

### Practical Example

```text
A developer creates a new GitHub repository and selects:
- Add a README file
- Add a .gitignore file
- Choose an MIT license
```

After the repository is created, GitHub automatically generates those selected files.

The `package.json` file would still need to be created separately for a Node.js application.

---

## Question 03

Which of the following Git commands is used to clone a remote repository to your local computer?

### Answer

`git clone`

### Explanation

The `git clone` command creates a local copy of a remote repository on your computer.

When cloning a repository, Git downloads:
- project files
- commit history
- branches
- repository configuration

This allows developers to work on the project locally while staying connected to the remote repository hosted on platforms such as GitHub.

Cloning repositories is a common workflow in collaborative software development.

### Practical Example

```bash
git clone https://github.com/user/project.git
```

After running the command, Git creates a local copy of the repository:

```text
project/
├── README.md
├── src/
├── assets/
└── .git/
```

Developers can then edit files, create commits and push changes back to the remote repository.