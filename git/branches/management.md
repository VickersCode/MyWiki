# Branch Management
[Table of Contents](../../README.md) | [Markdown Cheatsheet](../../Markdown%20Cheatsheet.md)

credit: [https://git-scm.com/book/en/v2](https://git-scm.com/book/en/v2)
___

#### Common Commands

Using just `git branch` lists all of the current branches associated with the project.

```console
$ git branch
  iss53
* master
  testing
```

the \* signifies which branch we currently have checked out (i.e. where the HEAD points)

We can see the last commit on each branch by using 
```console
$ git branch -v
```

Using the --merged or --no-merged options, we can see which branches have or have not merged into the branch we are currently working.
```console
$ git branch --merged
$ git branch --no-merged
```
This could be useful to help us determine if it's okay to delete a branch or not.

#### Changing Branch Name


