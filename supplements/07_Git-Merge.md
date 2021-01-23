Remember that the purpose of a topic branch is that it lets you make changes that do not affect the master branch. Once you make changes on the topic branch, you can either decide that you don't like the changes on the branch and you can just delete that branch, or you can decide that you want to keep the changes on the topic branch and combine those changes in with those on another branch.

Combining branches together is called **merging**.

Git can automatically merge the changes on different branches together. This branching and merging ability is what makes Git _incredibly powerful_! You can make small or extensive changes on branches, and then just use Git to combine those changes together.

It's very important to know which branch you're on when you're about to merge branches together. Remember that **making a merge makes a commit**.

Let's see how this works, in theory. Pay attention to the two main types of merges in Git, a `regular merge` and a `Fast-forward merge`.

# The Merge Command
The `git merge` command is used to combine Git branches:
```sh
$ git merge <name-of-branch-to-merge-in>
```

When a merge happens, Git will:
* look at the branches that it's going to merge
* look back along the branch's history to find a single commit that both branches have in their commit history
* combine the lines of code that were changed on the separate branches together
* makes a commit to record the merge

## Perform A Fast-forward Merge
* the branch being merged in must be ahead of the checked out branch. The checked out branch's pointer will just be moved forward to point to the same commit as the other branch.

## Perform A Regular Merge
* two divergent branches are combined
* a merge commit is created
