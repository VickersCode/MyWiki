# Intro
[Table of Contents](/README.md) | [Markdown Cheatsheet](/Markdown%20Cheatsheet.md)

credit: [https://git-scm.com/book/en/v2](https://git-scm.com/book/en/v2)
___

Branching allows us to edit code without messing with the main product. Imagine screwing up a project with thousands of lines of code - to the point where we need to start over. Branching alleviates this.

Git stores its data as a series of snapshots. When we commit, an object is stored containing a pointer to the snapshot as well as the author, message, etc. Each commit stores a pointer to the previous commit. 

A branch is a movable pointer to the most recent commit. Every time we make a commit, the branch automatically forwards the pointer.