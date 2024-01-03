# Rebase
[Table of Contents](../../README.md) | [Markdown Cheatsheet](../../Markdown%20Cheatsheet.md)

credit: [https://git-scm.com/book/en/v2](https://git-scm.com/book/en/v2)
___

[more information here](https://git-scm.com/book/en/v2/Git-Branching-Rebasing)

`git rebase` is the counterpart to `git merge`. Each have their use cases.

When we use `git merge`, it takes the endpoints and merges them together. 
When we use `git rebase`, we take all the changes committed from one branch and replay them on another. This is useful, for example, on projects that we are contributing to, but do not maintain. 

>[!WARNING]
>**Do not rebase commits that exist outside your repository and that people may have based work on.**

