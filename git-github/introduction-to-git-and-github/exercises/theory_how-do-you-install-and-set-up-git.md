## Module Overview

This module teaches how to install Git on Linux, Windows, and macOS. On most Linux distributions, Git usually comes pre-installed. The module also explains how to configure your Git username and email address.

## Question 01

What does the following command do?

![Git Config Diagram](../../assets/images/git-config.png)

### Answer

Shows your current Git configuration settings and where they are stored on your system.

### Explanation

The `git config --list --show-origin` command displays all configured Git settings, including the file where each configuration is defined.

Git stores configuration settings in different levels:
- system
- global
- local

This command helps developers understand:
- which settings are active
- where they were configured
- how Git is currently configured on the machine

It is especially useful for troubleshooting configuration issues or verifying user information such as username and email.

### Practical Example

```bash
git config --list --show-origin
```

Example output:

```text
file:C:/Program Files/Git/etc/gitconfig core.editor=vim
file:C:/Users/user/.gitconfig user.name=USER
file:C:/Users/user/.gitconfig user.email=user@example.com
```

In this example:
- the editor configuration comes from the system configuration file
- the username and email come from the global user configuration file

## Question 02

What is the purpose of using the `--global` flag when configuring your user name?

### Answer

The `--global` flag is used to configure the Git user name for all repositories on your system.

### Explanation

Git allows configuration settings to be applied at different levels:
- system
- global
- local

When using the `--global` flag, the configuration is stored in the global Git configuration file associated with the current user account.

This means the configured user name will automatically be used in all Git repositories created or used by that user on the machine.

Without the `--global` flag, the configuration would only apply to the current repository.

This setting is important because Git uses the configured user name to identify who created each commit in the project history.

### Practical Example

```bash
git config --global user.name "user"
```

After running this command, all future commits created on the system will use the configured user name unless a different local configuration is defined for a specific repository.

## Question 03

Which of the following is NOT a valid option mentioned for setting your preferred editor in Git?

### Answer

ESLint

### Explanation

Git allows developers to configure a preferred text editor that will be used for tasks such as:
- writing commit messages
- editing configuration files
- resolving merge conflicts

Common editors that can be configured in Git include:
- Vim
- Nano
- VS Code

ESLint is not a text editor. It is a static code analysis tool used to identify and fix problems in JavaScript and TypeScript code.

Because of this, ESLint cannot be used as a Git editor configuration option.

### Practical Example

```bash
git config --global core.editor "code --wait"
```

This command configures Visual Studio Code as the default Git editor.

Another example using Nano:

```bash
git config --global core.editor "nano"
```

