# Debugging with git bisect

## Learning objectives

- Use the git bisect command for debugging.
- Understand the importance of thoughtful, intentional problem-solving.

### Estimated time: 0.5h

## Description

You are already familiar with the concept of debugging. You have learned about it in [the previous module](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/debugging/debugging_and_developer_tools.md) or during building your projects in Microverse 1.0.
Most likely, you had to debug your code while building your web apps, and you know that sometimes it is really difficult to discover what is causing some unexpected behavior.
In this lesson you will learn about a tool that can help you find out in which commit a bug was introduced.

### Why is git bisect important?

The `git bisect` command is a way to make your investigations faster. Especially in the case of big projects, finding when and why a bug was introduced can be a neverending story.

### Learn more about git bisect

`git bisect` uses binary search (spoiler alert - you will learn about it in a few weeks!) to find the commit that introduced a bug.
Right now, you do not need to understand the theory behind binary search fully.
Please focus on understanding how to use `git bisect` - after learning `git bisect`, understanding binary search will be a piece of cake for you!

- Read the article [Debug your code using git bisect](https://codeburst.io/debug-your-code-using-git-bisect-45db2983cc69) by Nayeem Reza.
- Watch it in action in the [Git bisect tutorial - How to find a bad bug commit](https://www.youtube.com/watch?v=D7JJnLFOn4A&t=6s) by Ihatetomatoes.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
