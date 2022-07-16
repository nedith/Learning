# Catch hidden bugs!

## Learning objectives

- Locate a bug using manual QA methods.
- Clone an existing repository.
- Use the git bisect command for debugging.
- Understand the importance of thoughtful, intentional problem-solving.

### Estimated time: 1h

## Exercise

In this exercise, you will find and fix a couple of bugs.

*IMPORTANT NOTE: Read **all** instructions before you start this exercise.*

### Instructions

- Clone [curriculum-tools-buggy-restaurant](https://github.com/microverseinc/curriculum-tools-buggy-restaurant).
- Run the project on your local machine according to the instructions in its README file. Make sure that you can open the website in your browser.

#### Bug #1
- The bug is described as:
    - Current behavior: as a user, when I click the "Contact" link in the navigation, nothing happens.
    - Expected behavior: as a user, when I click the "Contact" link in the navigation, I am taken to to a page with restaurant contact information.
- Reproduce the bug in your local version of the project.
- Use the ` git bisect` command to find out in which commit a bug was introduced.
- Fix the bug! ❌🐛
- _There is no need to commit your changes now._
- Verify that website behaves in an expected way after your fix.

#### Bug #2
- The bug is described as:
    - Current behavior: as a user, when I open the menu page, I can see menu items overlapping.
    - Expected behavior: as a user, when I open the menu page, I can see menu items ordered into two columns and two rows.
- Reproduce the bug in your local version of the project.
- Use the ` git bisect` command to find out in which commit a bug was introduced.
- Fix the bug! ❌🐛
- _There is no need to commit your changes now._
- Verify that website behaves in an expected way after your fix.

#### 5-minute long video
Once you know the solution for two bugs, prepare a short video about them.

- First, undo your changes.
- Record a [loom video](https://www.loom.com/) that will show (for one of the bugs you found):
    - How you reproduce the bug in your local environment.
    - How you locate the commit that introduced the bug by using `git bisect`.
    - How you fix the bug.
    - How you verify that bug is gone.
- Your video should not be longer than 5 minutes.
- The link to the loom video should be submitted as the outcome of this exercise.
- _Please do not share your video or code with other students! Let them have fun with bugs!_

### Submit your exercise

[Read this FAQ for a reminder on how to submit your exercise.](https://microverse.zendesk.com/hc/en-us/articles/360061344234)

Now go to your Student Dashboard and submit your exercise.
Paste a link to the loom video you have recorded.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
