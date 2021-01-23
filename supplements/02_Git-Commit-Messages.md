# Good Commit Messages
Let's take a quick stroll down Stickler Lane and ask the question:

> How do I write a good commit message? And why should I care?

These are _fantastic_ questions! I can't stress enough how important it is to spend some time writing a _good_ commit message.

Now, what makes a "good" commit message? That's a great question and has been written about a number of times ([Link1](https://chris.beams.io/posts/git-commit/), [Link2](https://p5v.medium.com/what-s-with-the-50-72-rule-8a906f61f09c#.jwprsco0n), [Link3](https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)). Here are some important things to think about when crafting a good commit message:

## Do
* do keep the message short (less than 60-ish characters)
* do explain what the commit does (not how or why!)

## Do not
* do not explain why the changes are made (more on this below)
* do not explain how the changes are made (that's what `git log -p` is for!)
* do not use the word "and"
  * if you have to use "and", your commit message is probably doing too many changes - break the changes into separate commits
  * e.g. "make the background color pink and increase the size of the sidebar"
The best way that I've found to come up with a commit message is to finish this phrase, "This commit will...". However, you finish that phrase, use that as your commit message.

Above all, **_be consistent_** in how you write your commit messages!


