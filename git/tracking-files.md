[Table of Contents](../README.md) | [Markdown Cheatsheet](/Markdown%20Cheatsheet.md)
___
## `git add` 

`git-add` stages a file to begin tracking. According to the git docs, `git-add` could be read as:

> "Add precisely this content to the next commit"

So any changes made will reside here until ready to commit.

Once a file has been tracked, can skip the `git add` phase by using

`git commit -a -m "message"`

___
## `git commit`

Usually runs as `git commit -m "text about commit here"`

Takes everything from staging area and makes a permanent snapshot of the current state to the repository.

Every time you run `git commit` a snapshot is saved that the project can be reverted to later
___
## `git push`

This adds the changes from the git repository to the repository on GitHub
Changes are "final", although there are previous snapshots in case things break
___

![git add commit](../images/git-add-commit.png)