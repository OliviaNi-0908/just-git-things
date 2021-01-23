# Why Do We Need This
You might be like me where I start work on the next feature to my project at night, but then go to bed before I actually finish. Which means that, when I start working the next day, there are uncommitted changes. This is fine because I haven't finished the new feature, but I can't remember exactly what I've done since my last commit. `git status` will tell us what files have been changed, but not what those changes actually were.

The `git diff` command is used to find out this information!


# git diff
The git diff command can be used to see changes that have been made but haven't been committed, yet.

```sh
$ git diff
```

The output of the `git diff` command is the same output that we say with `git log -p`! Wanna know a secret? `git log -p` uses git diff under the hood.
