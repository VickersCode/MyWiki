[Table of Contents](../README.md) | [Markdown Cheatsheet](/Markdown%20Cheatsheet.md)
credit: [https://git-scm.com/book/en/v2](https://git-scm.com/book/en/v2)

___

## Removing Files

##### `git rm <filename>`

Moves a file from "changes to be committed" to "changes not staged for commit"

If there is an error, because of modifications to the file before removal or already added to the staging area, a force removal with the `-f` flag should help, but be careful.
___

## Moving Files

From the git book,

> "Unlike many other VCSs, Git doesn’t explicitly track file movement. If you rename a file in Git, no metadata is stored in Git that tells it you renamed the file. However, Git is pretty smart about figuring that out after the fact — we’ll deal with detecting file movement a bit later.

>Thus it’s a bit confusing that Git has a `mv` command. If you want to rename a file in Git, you can run something like:

```console
$ git mv file_from file_to
```
"

Basically, this is the best way to rename a file.