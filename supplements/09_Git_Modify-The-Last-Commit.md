# Changing The Last Commit
You've already made plenty of commits with the `git commit` command. Now with the `--amend` flag, you can alter the _most-recent_ commit.
```sh
$ git commit --amend
```

* If your Working Directory is clean (meaning there aren't any uncommitted changes in the repository), then running `git commit --amend` will let you provide a new commit message. (e.g. fix a misspelling commit message)
* Alternatively, `git commit --amend` will let you include files (or changes to files) you might've forgotten to include.
  * edit the file(s)
  * save the file(s)
  * stage the file(s)
  * and run `git commit --amend` to update the most-recent commit instead of creating a new one.

