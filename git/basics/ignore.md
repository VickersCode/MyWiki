[Table of Contents](README.md) | [Markdown Cheatsheet](/Markdown%20Cheatsheet.md)
credit: [https://git-scm.com/book/en/v2](https://git-scm.com/book/en/v2)

___

a `.gitignore` file is used to list files that we want git to ignore, like temp files created by Emacs, for example.

the following code reads a `.gitignore` file, lists all files that end in an 'o' or an 'a', and all files that end in a '~' (like temp files created by Emacs)


```console
$ cat .gitignore
*.[oa]
*~
```

##### Here's another example of a `.gitignore` file:

```
# ignore all .a files
*.a

# but do track lib.a, even though you're ignoring .a files above
!lib.a

# only ignore the TODO file in the current directory, not subdir/TODO
/TODO

# ignore all files in any directory named build
build/

# ignore doc/notes.txt, but not doc/server/arch.txt
doc/*.txt

# ignore all .pdf files in the doc/ directory and any of its subdirectories
doc/**/*.pdf
```
