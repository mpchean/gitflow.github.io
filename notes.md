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

      !! Note - create another feature branch and repeat the process.