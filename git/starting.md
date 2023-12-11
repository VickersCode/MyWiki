## git-init 

A common boilerplate, once a repository has been created on GitHub: (Just change anywhere it says "title")

```
  echo "# title" >> README.md
  git init
  git add README.md
  git commit -m "first commit"
  git branch -M main
  git remote add origin https://github.com/VickersCode/title.git
  git push -u origin main
  ```

`git init` initializes an empty Git repository, which is a .git directory that holds refs/heads, refs/tags, etc, so that control is possible. 