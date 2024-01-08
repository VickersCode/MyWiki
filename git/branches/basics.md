# Git Basics
[Table of Contents](../../README.md) | [Markdown Cheatsheet](../../Markdown%20Cheatsheet.md)

credit: [https://git-scm.com/book/en/v2](https://git-scm.com/book/en/v2)
___

Branching and Merging allows us to fix issues on a separate branch, and then merge the fix once tests are adequate

#### Basic Branching

Say our company has issue \#69 within its issue-tracking system and we want to work on that. First, we create and switch to the branch using 
```console
$ git checkout -b iss69
```

which is the same thing as using 
```console
$ git branch iss69
$ git checkout iss69
```

Here we can make changes, which will only exist in the issue \#69 branch. Committing the changes does not, however, update the production build. 

#### Basic Merging

If the issue has been fixed, we can run the `git merge` command

```console
$ git checkout master
Switched to branch 'master'
$ git merge iss69
Merge made by the 'recursive' strategy.
index.html |    1 +
1 file changed, 1 insertion(+)
```

And then we can delete the iss69 branch because it is no longer needed.
```console
$ git branch -d iss53
```

#### Merging Conflicts

If we change the same part of a file differently in two branches, Git wouldn't know what to do. `git status` could help find where the discrepancies are.

There is also a useful GUI for `git merge`
```console
$ git mergetool
```

