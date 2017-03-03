### You Just Want That One Commit

Cherry picking allows you to pick up a commit from your reflog or another branch of your project and move it to your current branch. Right now, your file directory and log should look like this:

```sh
$ ls
README.md
$ git log --oneline
84nqdkq initializing repo with README
```

Let's cherry pick the commit where we added file 4:

1. Find the commit ID where you added file4.md: `git reflog`
-  Cherry-pick that commit: `git cherry-pick <SHA>`

Now when you view your directory and log, you should see:

```sh
$ ls
file4.md
README.md
$ git log --oneline
eanu482 adding file 4
84nqdkq initializing repo with README
```

Is the commit ID the same as the one you used in the cherry pick command? Why or why not?

> **Warning:** Remember, when using any commands that change history, it's important to make these changes before pushing to GitHub. When you change a commit ID that has been pushed to the remote, you risk creating problems for your collaborators.