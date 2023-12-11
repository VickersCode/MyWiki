## git-clone

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

git-clone is used to clone a repository into a newly created directory. It creates remote tracking branches, visible using `git branch --remotes`. After this, only `git fetch` and `git pull` are necessary.

Here is what it looks like to clone the repository that this wiki will exist in:

`git clone https://github.com/VickersCode/MyWiki`

## git-fetch

