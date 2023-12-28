# Intro
[Table of Contents](../../README.md) | [Markdown Cheatsheet](../../Markdown%20Cheatsheet.md)

credit: [https://git-scm.com/book/en/v2](https://git-scm.com/book/en/v2)
___

Branching allows us to edit code without messing with the main product. Imagine screwing up a project with thousands of lines of code - to the point where we need to start over. Branching alleviates this.

Git stores its data as a series of snapshots. When we commit, an object is stored containing a pointer to the snapshot as well as the author, message, etc. Each commit stores a pointer to the previous commit. 

A branch is a movable pointer to the most recent commit. Every time we make a commit, the branch automatically forwards the pointer.

___
### Creating a Branch

`git branch testing` creates a new branch called testing, which is basically another pointer for us to move around. At this point, it is pointing to the same commit we are already on, which is pointing to the commit before that, which is pointing to the commit before that, etc, etc. This only created the branch, though.

![HEAD to master](../../images/head-to-master.png)

As we can see from the image above, there is a pointer called HEAD which points at the local branch we are currently working in. 

We can use the `git log` command with a `--decorate` tag to show which branch we are pointed at.

```console
$ git log --oneline --decorate
f30ab (HEAD -> master, testing) Add feature #32 - ability to add new formats to the central interface
34ac2 Fix bug #1328 - stack overflow under certain conditions
98ca9 Initial commit
```

___
### Switching Branches

```console
$ git checkout testing
```

This command moves us to the testing branch, so now HEAD is pointing at testing rather than master. Once a commit has been made on the testing branch, our pointers will look like this. 

![New pointers](../../images/commit-testing.png)

Master remained where it was, and testing pointed forward. If we were to `git checkout master`, HEAD would point to master and we would be working on the project up to that point, in case we want to move forward in a different direction than the testing branch went. 

If we commit from the master at this point, the project will be forked in two different directions, which can be merged. 