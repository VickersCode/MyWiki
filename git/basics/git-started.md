[Table of Contents](README.md) | [Markdown Cheatsheet](/Markdown%20Cheatsheet.md)
credit: [https://git-scm.com/book/en/v2](https://git-scm.com/book/en/v2)

***
# git init

A common boilerplate, once a repository has been created on GitHub: (Just change anywhere it says "title")

```
  echo "# title" >> README.md
  git init
  git add README.md
  git commit -m "first commit"
  git branch -M main
  git remote add origin https://github.com/VickersCode/title.git
  git push -u origin main
  ```

`git init` initializes an empty Git repository, which is a .git directory that holds refs/heads, refs/tags, etc, so that control is possible. 

___

# git status

Files are untracked until `git add` stages them for tracking.
This is useful so we don't accidentally add binary files to the repository, for instance, by running `git add .` . We can check the files staged for commit before we push changes.

### `git status -s` (A shorthand flag)

| Symbol | Description |
| -----| ---------------------------|
| ?? | Untracked files |
| A | New files to staging area |
| M | Modified files |
| MM | Modified w/ changes |

