[Table of Contents](../README.md) | [Markdown Cheatsheet](/Markdown%20Cheatsheet.md)
___
## `git clone`

Only need to use `git clone` once. Afterwards, `git pull` will be most common.

```
_git clone_ [--template=<template-directory>]
	  [-l] [-s] [--no-hardlinks] [-q] [-n] [--bare] [--mirror]
	  [-o <name>] [-b <name>] [-u <upload-pack>] [--reference <repository>]
	  [--dissociate] [--separate-git-dir <git-dir>]
	  [--depth <depth>] [--[no-]single-branch] [--no-tags]
	  [--recurse-submodules[=<pathspec>]] [--[no-]shallow-submodules]
	  [--[no-]remote-submodules] [--jobs <n>] [--sparse] [--[no-]reject-shallow]
	  [--filter=<filter> [--also-filter-submodules]] [--] <repository>
	  [<directory>]
```

`git-clone` is used to clone a repository into a newly created directory. It creates remote tracking branches, visible using `git branch --remotes`. After this, only `git fetch` and `git pull` are necessary.

Here is what it looks like to clone the repository that this wiki will exist in:

#### `git clone https://github.com/VickersCode/MyWiki`

___

## `git fetch`

`git fetch` gathers the commits that do not exist and stores them in the local repository **without** merging them to the current branch. 

Useful for keeping code up to date, but working on something that may break.


___


## `git pull`

`git pull` automatically merges after fetching commits. Basically, runs a `git merge` after a `git fetch`

For example, I currently have 3 workstations for this project, depending if I'm at work or home. First thing I do is run `git pull` to grab the most up to date commit from the repository. 
