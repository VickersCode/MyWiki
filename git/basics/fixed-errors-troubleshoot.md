[Table of Contents](README.md) | [Markdown Cheatsheet](/Markdown%20Cheatsheet.md)
credit: [https://git-scm.com/book/en/v2](https://git-scm.com/book/en/v2)

___
## Cannot `git pull` because of override error:
![overwrite error](overwrite-error.png)

Run `git stash` to store the changes elsewhere. Then you can run `git pull` to pull the repository and `git stash drop`to remove the old files:\
![overwrite error solution](overwrite-error-solution.png)
___
