[Table of Contents](/README.md) | [Markdown Cheatsheet](/Markdown%20Cheatsheet.md)

credit: [https://git-scm.com/book/en/v2](https://git-scm.com/book/en/v2)
___
Remote repositories exist on the internet or a network somewhere, hence the name "remote". This allows us to work on projects as a team, or at multiple workstations. 

#### Showing Remotes

Just run `git remote` to show a list of each remote handle associated with the project. `origin` is the default, so that should always show.

Using the `git remote -v` flag will show a list of URLs that Git has stored for reading (fetch) and writing (push)

#### Adding Remotes

`git remote add <shortname> <url>` adds a new remote repository. (origin = shortname)

Now, we can just use the shortname instead of the full URL. For example, 

```console
$ git fetch pb
remote: Counting objects: 43, done.
remote: Compressing objects: 100% (36/36), done.
remote: Total 43 (delta 10), reused 31 (delta 5)
Unpacking objects: 100% (43/43), done.
From https://github.com/paulboone/ticgit
 * [new branch]      master     -> pb/master
 * [new branch]      ticgit     -> pb/ticgit
```

#### Inspecting Remotes

`git remote show <remote>` will give more information about a particular remote. 

#### Rename/Remove

```console
$ git remote rename pb paul
$ git remote
origin
paul
```

```console
$ git remote remove paul
$ git remote
origin
```

