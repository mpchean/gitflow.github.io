# [Git Workflows](https://www.linkedin.com/learning/git-workflows/collaborating-more-effectively-with-git-using-workflows?autoplay=true)

1. Git Workflows are an agreement between developers that defines and standardizes hwo source code is shared and how it is managed.
2. Developer needs to merge code - Team needs to sync code changes - CI - needs to build and deploy code.  Emergency hot fixes.
3. Basic building blocks.
  a. Shared repository.
  b. Local repository.  Where developer works on code.
  c. Types of branches. 
      i. Long lived branches - main branch.  Develop branch.  
      ii. Short lived branches. Opened for single purpose then closed.  Feature branch. Hotfix branch. 
4. *Pull* request a feature that allows other tem members to inspect code changes before being *Merged*.
5. Workflow selection.
   a. Team size. 
      i. Small team - use a workflow that is more focused on the individual work. Conducive to streamlining.
      ii. Large team - use a workflow that is more focused on the team work. Conducive to collaboration. More structure in workflow.
   b. Release Cadence
      i. Slower - Monthly or Quarterly - more long lived branches
      ii. Faster - Daily or Hourly - more short lived branches
   c. Automation 

   ## Gitflow Model
   1. Slower release viable option
   2. 2 branches main & develop
   3. main holds the code that is production ready state and can be release
   4. Develop stores the latest dev changes for the next release.
      - When this code reaches a stable level it will then be placed into the develop branch.
   5. Steps to implementing
      a. Create the develop branch in the repository
      b. git checkout -b develop origin/develop
      c. Create a feature branch.   git checkout -b feature/mc-123-site-content
      d. Make changes
      e. git add .
      f. git commit -m "Add new content"
      g. git push origin feature/mc-123-site-content -u
      h. Create a pull request making sure that the base is the develop branch.
      i. Then merge the branch.

   ## creating a release
   1. Create a release branch from the develop branch.
   2. Make small changes only to the branch while it is being tested.
     - this allows the dev team to contiue working with the dev branch while the release is being tested.
   3. The release branch is then merged into the main branch

   ## Hotfixes
   1. Create a hotfix branch from the main on Github. 
   2. Make your changes and commit changes
   3. Then create pull request into main & merge
   4. Create new pull request and merge hotfix into the develop branch.

   ## GitHub Flow
   1. More streamlined that Git Flow
   2. Main is only long-lived branch.
   3. Does not use develop, release or hotfix branches.
   4. Designed for higher cadence releases
   5. Developer creates feature branch off of main branch.
   6. When a milestone is reached the feature branch is pushed up to remote but no pull request is created.
   7. when the feature branch is finished then it is uploaded and a pull request is created.
   8. Get rid of all branches in github besides main.
   9. git checkout main to make sure local main branch is up to date.
   10. git pull will sync main
   11. create a new branch from main with git checkout -b feature/mc-something
   12. make changes to the branch
   13. git add then commit 
      !! Note - create another feature branch and repeat the process