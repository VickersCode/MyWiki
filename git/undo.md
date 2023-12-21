[Table of Contents](../README.md) | [Markdown Cheatsheet](/Markdown%20Cheatsheet.md)
___

Always keep in mind, it is not always possible to undo an undo. So going through these steps should be taken carefully.

If a project has been staged, but forgot to stage a file or files, or an edit, we can stage again and commit again using 
`git commit --amend`

Here's a short example
```console
$ git commit -m 'Initial commit'
$ git add forgotten_file
$ git commit --amend
```

The second commit replaces the first.
___

### Unstaging

Remember `git status`? If not, [here](./git-started.md#git%20status)

```console
$ git add *
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

    renamed:    README.md -> README
    modified:   CONTRIBUTING.md
```

But maybe we want to unstage CONTRIBUTING.md. In parenthesis in the code above, it says use "git reset HEAD \<file\>..." to unstage, so let's do that.

```console
$ git reset HEAD CONTRIBUTING.md
Unstaged changes after reset:
M	CONTRIBUTING.md
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

    renamed:    README.md -> README

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

    modified:   CONTRIBUTING.md
```

There we go.
