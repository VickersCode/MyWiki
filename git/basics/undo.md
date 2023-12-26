[Table of Contents](README.md) | [Markdown Cheatsheet](/Markdown%20Cheatsheet.md)
credit: [https://git-scm.com/book/en/v2](https://git-scm.com/book/en/v2)

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

Remember `git status`? If not, [here](git-started.md#git%20status)

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

____

### Unmodify

Using `git checkout --<file>` will revert a file to the latest staged or committed version. So things will be lost, be careful.

Stashing and branching may be a better way to go, especially for bigger team projects.

___
### git restore

`git restore` replaces `git reset` on Git version 2.23.0 onwards.

Luckily, the command is right there for us when we run `git status`
```console
$ git add *
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   CONTRIBUTING.md
	renamed:    README.md -> README
```

It says to use `git restore --staged <file>`
Once we run this, the file is still modified, but unstaged.

> [!WARNING]
> `git restore --staged <file>` is different than just running `git restore <file>` Which removes any local changes to that file.




