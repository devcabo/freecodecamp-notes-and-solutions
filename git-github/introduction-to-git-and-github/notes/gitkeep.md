## Notes

Git does not track empty folders.

If a directory does not contain any files, Git will ignore it and the folder will not be included when using `git push`.

To keep an empty folder in the repository, it is common practice to create a placeholder file such as:

```text
.gitkeep