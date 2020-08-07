# README

**A Repo where we get to submit pull requests for practice**<br>
**Credit to https://github.com/rmklaus12**

Don't know how? I'll show you! 



**Get the repo**
Start your contributing journey with us by forking this repo using the Fork button in the top-right corner of this screen. You should then be able to use git clone to copy your fork onto your local machine.

```bash
    git clone https://github.com/YOUR_GITHUB_USERNAME_HERE/PullRequest-Practice
```

Jump into your new local copy:

```bash
    cd all-about-git
```

And then add an `upstream` remote that points to the main repo:

```bash
    git remote add upstream https://github.com/aar9nk/PullRequest-Practice
```

Fetch the latest version of `master` from `upstream` (ie. the main repo):

```bash
    git fetch upstream master
```
**Making changes**

Make your changes on your computer using your favourite code editor.

Once you begin work on a particular issue, you should create a feature branch to make your changes. This keeps your master branch clean and also allows you to work on multiple issues at the same time and prevent any conflicts.

```bash
    git branch <your-branch-name> #creates a new branch
    git commit -m "Add a concise commit message describing your change here"
```

Once you've made your changes, you can commit.

```bash
    git add .
    git commit -m "Add a concise commit message describing your change here"
```

Push your changes to a branch on your fork:

```bash
    git push origin branch-name-here
```

**Commits**

_Keep your commit history clean, tidy and up-to-date_

Your commit history should contain only commits that are relevant to the change you are making. If you find that the list of commits for your PR contains commits that you did not make, then it is possible that you have accidentally merged something into you branch that you shouldn't have. Using `git rebase -i` to clean up your commit history and keep up to date.

_Commit messages should..._

-   be as short as possible, while providing enough detail to understand what is happening and why the change is being made
-   begin with a capital letter, and should not contain a full stop
-   ideally begin with an imperative verb "Add...", "Update...", "Fix...", "Remove..."
-   not be overly simplified or not explanatory (eg. `Emergency save`, or `Debug enterprise controller`, or `Tidy up`)

**Pull Requests**

Most pull requests are solving one issue. It's useful to include the issue number in the pull request's name, for example `3727-add-content-aboutpage`.

_Provide an explanation of the problem you are solving_

When you create a PR, you have the opportunity to explain the changes you have made to the codebase, and the more detail you provide, the better. Mention the other issues in the repo that your PR is related to. Someone needs to review your contribution before is merged into the code base. Having lots of information about what they are looking at makes the job of a reviewer much easier, and means that feedback is likely to be faster. That means we can get your change merged as quickly as possible.

If you are the only one working on your PR, and you need to update your PR with upstream changes from the `master` branch, please use the `git rebase` tool, rather than `git merge`. This helps keep your commit history clean and readable, and therefore easier to understand. For example, on your local machine:

```bash
git fetch origin # updates origin/master
git checkout your-pr-branch
git rebase origin/master # rebases your changes on top of origin/master
git push your-fork your-pr-branch --force-with-lease # updates your PR, overwriting your previous changes
```
TL;DR

Use the GitHub website to submit a new pull request against upstream/master.

-   Keep your PR small, with a single focus
-   Maintain a clean commit history
-   Use a style consistent with the rest of the codebase
-   Before submitting, rebase your work on the current master branch


