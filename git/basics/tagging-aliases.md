# Tagging and Aliases
[Table of Contents](../../README.md) | [Markdown Cheatsheet](../../Markdown%20Cheatsheet.md)

credit: [https://git-scm.com/book/en/v2](https://git-scm.com/book/en/v2)
___

## Tagging

Tagging is a way to save certain points in a repository's history.
Often, these are the different "versions"

Use `git tag` to list the existing tags in Git. They will be listed in alphabetical order by default.

Large repos can have a lot of tags, so we can use `git tag -l <version>` to minimize the search. 

```console
$ git tag -l "v1.8.5*"
v1.8.5
v1.8.5-rc0
v1.8.5-rc1
v1.8.5-rc2
v1.8.5-rc3
v1.8.5.1
v1.8.5.2
v1.8.5.3
v1.8.5.4
v1.8.5.5
```

There are two types of tags:
1. Lightweight
	- Pointer to a specific commit
2. Annotated
	- Checksummed 
	- Contains more information (email, date, tagging message)
	- Can be signed and verified with GNU GPG


#### Lightweight Tags

Tags without much information (not recommended by Git)\
To create, `git tag <tag-name>`

```console
$ git tag v1.4-lw
$ git tag
v0.1
v1.3
v1.4
v1.4-lw
v1.5
```

#### Annotated Tags

To create, specify the `-a` tag.

```console
$ git tag -a v1.4 -m "my version 1.4"
$ git tag
v0.1
v1.3
v1.4
```

The tagging message is stored with the tag, use `git show` to see it.


#### Tagging Previous Snapshots

If we want to tag a previous snapshot, we first need to get the checksum.

```console
$ git log --pretty=oneline
15027957951b64cf874c3557a0f3547bd83b3ff6 Merge branch 'experiment'
a6b4c97498bd301d84096da251c98a07c7723e65 Create write support
0d52aaab4479697da7686c15f77a3d64d9165190 One more thing
6d52a271eda8725415634dd79daabbc4d9b6008e Merge branch 'experiment'
9fceb02d0ae598e95dc970b74767f19372d61af8 Update rakefile
```

Then, we can use the first few characters of the checksum of the commit we want to tag.

```console
$ git tag -a v1.2 9fceb02
```

### Pushing Tags

Tags have to be pushed to the remote server separately, using \
`git push origin <tagname>`

We can also push all tags at once using `--tags`\
`git push origin --tags`

#### Deleting Tags

`git tag -d <tagname>` (This doesn't delete from the server though)

To delete from the server
```console
$ git push origin --delete <tagname>
```

### Checking Out Tags

```console
$ git checkout v2.0.0
Note: switching to 'v2.0.0'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 99ada87... Merge pull request #89 from schacon/appendix-final

$ git checkout v2.0-beta-0.1
Previous HEAD position was 99ada87... Merge pull request #89 from schacon/appendix-final
HEAD is now at df3f601... Add atlas.json and cover image
```

As we can see, checking out a tag puts our repository in "detached HEAD" state. We can make changes and commit, but the tag will be the same.

Best practice is to create a new branch.

____

## Aliases

Aliases make it so we don't need to type the full command to get something done. For example, if we want to type `git ci` instead of `git commit`, we need to run the following

```console
$ git config --global alias.ci commit`
```

A common alias allows us to easily view the latest commit

```console
$ git config --global alias.last `log -1 HEAD`
```









