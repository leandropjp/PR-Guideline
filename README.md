# Pull Request Guide
This document explains the guidelines for using Pull Requests on our projects.
### What is a Pull Request?
A Pull Request (PR) is a way of informing other developers about changes that you did on a development project. When you create a PR, members of your team can see your code, comment and suggest changes on specific lines. They can also choose to become reviewers of that PR, approving it or not.
### Creating a Pull Request on GitHub
To create a PR on GitHub, go to your project on the GitHub website and choose "New pull request". Select the branch in which you made your changes on the "compare" field and the branch that it will be merged to on the "base" field. After that, click "Create pull request".
### Keep your Pull Request short and understandable!
Please, use these guidelines:
1. [Separate subject from body with a blank line](https://chris.beams.io/posts/git-commit/#separate)
2. [Limit the subject line to 50 characters](https://chris.beams.io/posts/git-commit/#limit-50)
3. [Capitalize the subject line](https://chris.beams.io/posts/git-commit/#capitalize)
4. [Do not end the subject line with a period](https://chris.beams.io/posts/git-commit/#end)
5. [Use the imperative mood in the subject line](https://chris.beams.io/posts/git-commit/#imperative)
6. [Wrap the body at 72 characters](https://chris.beams.io/posts/git-commit/#wrap-72)
7. [Use the body to explain what and why vs. how](https://chris.beams.io/posts/git-commit/#why-not-how)

 ### Pull Request Guidelines
Our projects have 4 main branches:
- **Demo**: this branch is a mirror of the master branch. all hotfixes PR's should be done here; 
- **Master**: this is the current approved build. The master branch includes the most stable version of the code and any new release builds must be created based on this branch;
- **Staging**: this is the latest candidate build. A Staging build is supposed to go through QA and, once approved, will become the newest master build;
- **Development (Dev)**: this is the branch on top of which new features and overall changes to the code will be added;
- Before starting work on any new feature, modification or fix, the developer **must** create a new, separate branch that will be used solely for this specific task;
- In general, it will be created based on the **dev** branch.
- **Always** try to use the JIRA ID of the task in the branch name;
- If the developer is creating a branch for new feature, use the **dev** branch as base and the abbreviation `feat` in the branch name. For example: `feat/APP-144`;
- If the developer is creating a branch for a bug correction, use the **dev** branch as base and the abbreviation `bugfix` in the branch name. For example: `bugfix/APP-155`;
- If the developer is creating a branch for an improvement, use the **dev** branch as base and the abbreviation `enhc` in the name of the branch. For example: `enhc/APP-188`;
- If the developer is creating a branch for a bug correction with maximum priority and it is really necessary to update that fix as soon as possible, use the **demo** branch as base and the abbreviation `hotfix` in the name of the branch. For example: `hotfix/APP-199`;
- After finishing a task, the developer **must** create a PR so that the modifications will go through a review process before being merged;
- All merges, ideally, should be reviewed and approved by another member of the team;
- Once the PR is approved, the original developer is free to merge it and close the branch;
- When requested, the developer should create a PR from dev to staging and prepare a version from the Staging branch and send it to the QA Team. **Only applied for the front-end team**.

### Pull Request Creator Obligations
- **Keep PRs small!** If you feel that a specific task is becoming too big, try to divide it into smaller ones;
- **When necessary**, add a comment to every PR that you create explaining the code:
-- Your strategy to solve the issue;
-- Possible test cases;
-- If necessary, attach a picture of the feature/bugfix that you've made;
- What has been done on the PR (add a link to the Pivotal task when applicable);
- Make sure that your code follows the style guide for your language of choice;
- Your code is going to be seen by another developer, so strive to make it as clear as possible Be open-minded about suggestions made by reviewers;

### Pull Request Reviewer Obligations
- Keep in mind that you are as responsible for every PR that you review as the original creator of that PR;
- Make an effort to actually understand what was done on the PR;
- How would you feel if you had to work on top of this code on the future? Suggest changes, no matter how small or trivial they seem;
- Ensure that the style guide is being followed;
- Don't be afraid to hold off on approving a PR until you are satisfied with it;

### Using Git on your project
- Keep the commits clean;
- Don't commit unfinished code, use `stash` to save your code if you need to change branches;
- If you need to change something in your last commit, be it message, you can use `amend` to edit it. This should **NEVER** be done if the commit is on one of the 3 main branches and it was pushed to origin;
- If you need something from other branches but do not want the whole code, you can use `cherry pick` on specific commits, git will duplicate these commits in the current branch;
