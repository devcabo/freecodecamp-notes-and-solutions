## Module Overview

This module covers account authentication and the integration between Git and GitHub using SSH and GPG keys.

It also explains how authentication works through locally generated keys stored on the user's machine.

---

## Question 01

What is the fundamental difference between private and public keys in SSH and GPG key pairs?

### Answer

The private key stays on your local machine while the public key is shared.

### Explanation

SSH and GPG authentication systems use a pair of cryptographic keys:
- a private key
- a public key

The private key is stored securely on the developer's local machine and should never be shared with other people.

The public key can be uploaded to services such as GitHub to verify the identity of the user.

This authentication method improves security because passwords do not need to be transmitted during authentication.

SSH keys are commonly used for:
- authenticating GitHub access
- securely pushing and pulling repositories

GPG keys are commonly used for:
- signing commits
- verifying commit authenticity

### Practical Example

```text
A developer generates an SSH key pair on their computer.

The public key is uploaded to GitHub, while the private key remains stored locally on the machine.
```

After the setup process, GitHub can verify the developer's identity securely whenever Git operations are performed.

---

## Question 02

Which command would you use to enable automatic signing of all commits with your GPG key?

### Answer

```bash
git config --global commit.gpgsign true
```

### Explanation

Git supports commit signing through GPG keys to help verify the authenticity of commits.

When automatic signing is enabled:
- every commit is signed automatically
- commit authorship becomes verifiable
- repository security and trust are improved

The `--global` flag applies the configuration to all repositories used by the current user on the machine.

Signed commits are commonly used in professional and collaborative development environments.

### Practical Example

```bash
git config --global commit.gpgsign true
```

After running this command, Git automatically signs future commits using the configured GPG key.

Example commit:

```bash
git commit -m "docs: update authentication notes"
```

GitHub can then display the commit as a verified commit if the GPG key is properly configured on the account.

---

## Question 03

What's required to set up SSH key signing for Git commits on GitHub?

### Answer

Set the signing format to SSH and configure your signing key path.

### Explanation

Git supports SSH-based commit signing as an alternative to GPG signing.

To configure SSH signing, developers need to:
- define SSH as the signing format
- specify the SSH signing key path
- upload the public signing key to GitHub

This allows GitHub to verify that commits were created by an authenticated developer.

SSH signing helps improve:
- commit authenticity
- repository security
- developer identity verification

### Practical Example

```bash
git config --global gpg.format ssh
git config --global user.signingkey ~/.ssh/id_ed25519.pub
```

These commands configure Git to use SSH signing for commits.

After configuration, commits created by the developer can be verified by GitHub when the corresponding public key is added to the account settings.