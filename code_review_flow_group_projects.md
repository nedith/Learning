

# Code review flow for group projects at Microverse

## Step-by-step guide

### Phase 1: teammates' reviews

1. Once you are ready with the initial version of your task:
    - Open a pull request **from your feature branch to the development branch** with changes that need a review.
    - Move your task's card in the Kanban board to the "In review" column.
    - Ask your teammates for a code review.
2. Check if any of your teammates needs a code review:
   - Take a look at the "In review" column on the Kanban board.
   - Double-check to make sure that someone else isn't already performing a review.
   - As soon as you find a pull request to review, add a GH comment to that pull request saying that you have started that review.
3.  Once you get feedback about your task from your team member:
    - Remind yourself that feedback is a positive thing even if it feels a bit unpleasant.
    - Commit changes based on review comments. **Remember to use the same pull request as in your initial review.**
    - If you have any doubts about any of the comments, answer back in the pull request. Remember to ask specific questions because you might not get an answer immediately as a result of async communication.
    - When your changes are ready, ask your teammates for a re-review.
4. Once your pull request is approved by a team member:
   - Merge your pull request into the development branch.
   - Continue to the next task in your backlog.

### Phase 2: external code review

4. Once you are ready with all tasks and all pull requests are merged into the development branch:
    - Open a pull request **from the development branch to the main branch** with all changes made by your team.
    - Copy the link to the your pull request.
    - Go to the Student Dashboard's "View progress" page, find the name of the project you have finished and select 'Actions' -> 'Request Review'. Paste the link to your pull request.
5. While waiting for a code review:
     - Continue with the next activity.
6.  Once you get feedback about your project:
    - Remind yourself that feedback is a positive thing even if it feels a bit unpleasant.
    - Commit changes based on review comments. **Remember to use the same pull request as in your initial review.**
    - If you have any doubts about any of the comments, answer back in the pull request. Remember to ask specific questions because you might not get an answer immediately as a result of async communication.
    - When your changes are ready, go to your Student Dashboard and ask for a re-review. **Remember that you have a max of 3 reviews per project (for some more complex projects, it can be more, and you will see that in your Dashboard).**
7. Once your project is approved:
     - Merge your pull request into the main branch.
     - Go to your Student Dashboard and submit your project as completed.
     
## Visualization

Take a look at this chart that shows the process described above (note that phase 2 is the same as in [regular code review flow at Microverse](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/code-review/articles/how_to_ask_for_a_code_review.md)):

![code review flow for group project](../images/code_review_flow_group.png)

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
