# What If A Merge Fails?
The merges we just did were able to merge successfully. Git is able to intelligently combine lots of work on different branches. However, there are times when it can't combine branches together. When a merge is performed and fails, that is called a **merge conflict**.

If a merge conflict does occur, Git will try to combine as much as it can, but then it will leave special markers (e.g. `>>>` and `<<<`) that tell you where you (yep, you the programmer!) needs to **manually** fix.


# What Causes A Merge Conflict
As you've learned, Git tracks lines in files. A merge conflict will happen when the exact same line(s) are changed in separate branches.

# Merge Conflict Output Explained
For example, the output that shows in the Terminal is:
```sh
$ git merge heading-update 
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.
```

Notice that right after the `git merge heading-update` command, it tries merging the file that was changed on both branches (`index.html`), but that there was a conflict. Also, notice that it tells you what happened - "Automatic merge failed; fix conflicts and then commit the result".

Remember our good friend `git status`? We'll come in really handy when working with merge conflicts.
The `git status` output tells us to that the merge conflict is inside `index.html`, so let check out that file!


# Merge Conflict Indicators Explanation
The editor has the following merge conflict indicators:

* `<<<<<<< HEAD` everything below this line (until the next indicator) shows you what's on the current branch
* `||||||| merged common ancestors` everything below this line (until the next indicator) shows you what the original lines were
* `=======` is the end of the original lines, everything that follows (until the next indicator) is what's on the branch that's being merged in
* `>>>>>>> heading-update` is the ending indicator of what's on the branch that's being merged in (in this case, the `heading-update` branch)


# Resolving A Merge Conflict
Git is using the merge conflict indicators to show you what lines caused the merge conflict on the two different branches as well as what the original line used to have. So to resolve a merge conflict, you need to:
* choose which line(s) to keep
* remove all lines with indicators


# Commit Merge Conflict
Once you've removed all lines with merge conflict indicators and have selected what heading you want to use, just save the file, add it to the staging index, and commit it! And that's it! Merge conflicts really aren't all that challenging once you understand what the merge conflict indicators are showing you.

