# See All Branches At Once

Assume now we have multiple sets of changes on multiple different branches. We can't see other branches in the `git log` output unless we switch to a branch. Wouldn't it be nice if we could see all branches at once in the `git log` output.

As you've hopefully learned by now, the `git log` command is pretty powerful and can show us this information. We'll use the new `--graph` and `--all` flags:
```sh
$ git log --oneline --decorate --graph --all
```

The `--graph` flag adds the bullets and lines to the leftmost part of the output. This shows the actual branching that's happening. 
The `--all` flag is what displays all of the branches in the repository.

Running this command will show all branches and commits in the repository.

