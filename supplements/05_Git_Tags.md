# Adding A Tag To A Specifici Commit
You have to do is provide the SHA of the commit you want to tag!
```sh
$ git tag v1.0 a87984
```

this command will tag the commit with the SHA `a87084` with the tag `v1.0`. Using this technique, you can tag any commit in the entire git repository! Pretty neat, right?...and it's just a simple addition to add the SHA of a commit to the Git tagging command you already know.


# Verify Tag
So how do we know that a tag was actually added to the project? If you type out just `git tag`, it will display all tags that are in the repository.


# Deleting A Tag
What if you accidentally misspelled something in the tag's message, or mistyped the actual tag name (`v0.1` instead of `v1.0`). How could you fix this? The easiest way is just to delete the tag and make a new one.

A Git tag can be deleted with the `-d` flag (for delete!) and the name of the tag:
```sh
$ git tag -d v1.0
```
