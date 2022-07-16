# Resolve git conflict

## Learning objectives
- Solve simple git conflicts.

### Estimated time: 0.5h

## Exercise

In this exercice you will introduce git conflicts in the repo you created for practicing [Gitflow](https://github.com/microverseinc/curriculum-transversal-skills/tree/main/git-github/exercises/try_gitflow.md).
And then, you will resolve them!

*IMPORTANT NOTE: Read **all** instructions before you start this exercise.*

### Preparation - creating a merge confict

#### Making fixes in a new branch
- Make sure that you start from the `add-quotes` branch:
    - `git checkout add-quotes`
- Create a new branch `fix-quotes` and switch to it:
    - `git checkout -b fix-quotes`
- Make changes in your files:
     - Fix the typo in the quote about a good programmer (`crosing` should be `crossing`).
     - Remove the empty test.txt file.
     - Add a new simplicity.txt file with the following sentence:
         - "Simplicity is the soul of efficiency." - Austin Freeman
- Commit your changes.
- Push `fix-quotes` to GitHub:
    - `git push --set-upstream origin fix-quotes`.
- Open a new pull request (from `fix-quotes` to `dev` branch):
    <p>
     <img src="../images/fix-quotes-to-dev.png" alt="Pull request from fix-quites to dev branch" width="400px" />
    </p>
- Keep this pull request open.

#### Introducing changes in the first branch
- Make sure that you are in the `add-quotes` branch:
    - `git checkout add-quotes`
- Make a change in the quote about a good programmer:
    - add its author: `Doug Linder`
- Add a simplicity.txt file with the following sentence:
     - "Nature is pleased with simplicity. And nature is no dummy." - Isaac Newton
- Commit your changes.
- Push `add-quotes` to GitHub:
    - `git push --set-upstream origin add-quotes`.

#### Merging pull requests
- First, merge your pull request from the `fix-quotes` branch (it should be the pull request #2).
- Then, go to your pull request from the `add-quotes branch` (it should be the pull request #1).
- Merge option should be disabled, and you should see the list of conflicts.
  <p>
     <img src="../images/disabled-merge-conflict.png" alt="Merge button disabled due to conflicts" width="600px" />
  </p>

### Instructions

Now it is time to solve the conflict. Do it by using the command line.

- Make sure that your `dev` branch is up-to-date:
    - `git checkout dev`
    - `git pull`
- Switch to the `add-quotes` branch (if it is confusing to you, check [this issue](https://github.com/microverseinc/curriculum-transversal-skills/issues/83)):
    - `git checkout add-quotes`
- Try to merge the `dev` branch:
    - `git merge dev`
- You should see this message about a merge conflict:
    - "Automatic merge failed; fix conflicts and then commit the result."
- Check the status of your files to have clear information:
    - `git status`
- You should see the following message:
    <p>
     <img src="../images/conflict-command-line.png" alt="Conflict displayed in command line" width="400px" />
    </p>
- Open the conflicting files and decide which changes should stay.
- Commit your changes:
    - `git add <FILE NAMES>`
    - `git commit` (git is smart enough to create a merge commit message for you in this case)
- Push your changes to GitHub.
- Check your pull request. Now you should be able to merge your pull request from the `add-quotes` branch.

### Submit your exercise
[Read this FAQ for a reminder on how to submit your exercise.](https://microverse.zendesk.com/hc/en-us/articles/360061344234)
Now go to your Student Dashboard and submit your exercise.
Paste the link to your merged pull request from the `add-quotes` branch.


------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
