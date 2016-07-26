# Repository Orginization
*Rev 0.1-a*

------

## 1.0 Branching

Definition: branches are the substance of code on a Git repository, they are where your code lives and dies, looking at it from above a branch is essentially a timeline of what has happened to your code,

In the tradition Github workflow, the master branch is your always ready to deploy branch, meaning the code in there should be hard and battle tested, Essentially a workable version of whatever your project is attempting to create. For us, this is less effective due to both the number of commiters we are working with and the fact that all of us are working in the same repository with no forks. The best way for us to get around this is to create Three primary branches that are upgraded with new commits from a feature branch to demonstrate.
____________________________________
![Alt Text](http://i.stack.imgur.com/ZVqYX.png)
___________________________________

This diagram shows off the three branches that we will be using,
  - Master: Essentially where all the final tested code will go this branch should be as bug-free as possible and well documented, essentially the code on a robot during a competition should be from this branch.
  - Hotfix: This branch should be used whenever  there is a major bug in master that we can't wait to go through the other two branches before we deploy it, normally we do a lot of this at a competition where we need to make fixes in the robot quickly.
  - Release: Our testing phase all code that is deemed "Ready-To-Test" should go here, not really a long term storage branch, though.
  - Develope: This is the busiest of the branches any normal change to the code should start off being branched away from this, and then worked on in a feature branch until it is ready to come back into this branch. Most of the time new features will be pushed up from here to Release right away, this branch exists so there is another layer of security between master and any possible broken features.
  - Feature: where all the meat is made, 80% of all commits will come out of these branches, with each "Feature Branch" focusing on one particular subject, "Feature", or Issue.
***
## 2.0 Pulling

Definition: Pulling is the act of pulling code from a lower branch into a higher one, this could also be called a merge, but merges are generally only called then when coming down from a higher one into a lower.

In order to successfully close a pull request several things must happen, or two things really.
  1. A Mentor or Programming team lead must review the code being changed in the pull request to make sure it is up to the Style standards.
  2. The code must pass a Travis-CI build if the code cannot build then the code will not be pulled until a successful build can be completed.

At a feature to dev branch level, this is all that is needed the higher branches require a little more work.

In order to pull into the Release branch, the code must either fix some problem(ex. documentation, minor bugs), be able to close at least some part of an Issue.

In order to pull into the Develope branch, the code must have already done everything below it, as well as run successfully on the Robot, that it is designed to work on.
***
## 3.0 Issues

Issues are what we are trying to accomplish with our code, such as creating a new Shooter State Machine, or Implementing an acceleration profile, it can take a lot of different forms and entire careers are made of identifying and documenting issues. There are millions of solutions for issue trackers, from freeware like git-hub, to the top of the line thousand dollar enterprise solutions like Team-City, and Team Foundation Server, we will be using GitHub for several reasons, including the fact that it is free.

The most important part of an issue tracker are Labels and milestones.

### 3.1 Labels

Labels are what define an issue, what skills are needed to close it, how long it might take, what anyone else has done to solve this issue, the status of the issue going forward, should we even put any effort into solving the issue at the current time. All this information comes down to a few "simple" tags. The most important aspect of using GitHub issues is its ability to help us work together, if you are stuck with a certain part of an issue, leave a comment on it in GitHub, never be afraid to not know the answer, because even if we don't all know 100% of the solution to a problem, 100 people with 1% we get the same result. All that matters is that in the end we made a awesome robot.

  -  **Size tags:** Size of an issue can be solved in many ways, the top two methods are story-points, or just raw, time. Since in B.E.A.S.T. we don't often work in raw time it is easier for us to classify them by story points, each classification is based off of a team shirt size, and corresponds to the number of people needed and the number of meetings it will take to accomplish.
    - Extra-Small: 1 Person, Half a Meeting.
    - Small: 1 Person, 1 Meeting.
    - Medium: 1 Person, 2 Meetings.
    - Large: 2 People, 2 Meetings.
    - Extra-Large: 2 People, 2-5 Meetings.
    - Extra-Extra-Large: 2 People 5-10 Meetings.
    - Extra-Extra-Extra-Large: 2 Or more People, over 10 Meetings normally when problems become this large they need to be separated out into a larger number of smaller issues.

  - **Status Tags:** These tags denote the state of the issue, the two big ones are open and closed, but while an issue is open it can go through various stages.
    - Open: The open state can also be further refined to these more specific subcategories.
      - Not Started: No work has been done on this issue and no one is currently planning to work on it.
      - Committed: Someone is working on it.
      - Ready-To-Test: The Issue has been solved in code and now needs to be tested on a robot.
      - Ready-To-Pull: This issue is finished and tested and is ready to be pulled into the master branch.
    - Closed: Issue has been pulled into master and solves the issue.

  - **Type of Problem Tag**
    - Bug: A problem we discover in the master branch that needs to be patched.
    - Required: The robot needs this to work, without it, we would not be able to complete the challenge, an example is a drivetrain.
    - Enhancement: A feature that would make the robot better, but we could function without it.
    - Documentation: An issue around the state of our Documentation, this task could be something like writing a guide to a particular function of a robot, or going through others code.
    - WontFix: An issue that we know is there and we could work on but we won't, either because we don't have time to, it is so minor that fixing it really won't help, or it is something big that we can't address right now, like a major code rewrite.
  - **Area Tags**
    - This tag is pretty easy to figure out, as well as being pretty diverse in the areas it can cover, some examples are C#, and Java, being areas of code, but they could also be, UI, UX, Controls, Architecture.

### 3.2 Milestones
Milestones are a way to measure both the speed at which we are completing issues and also a way to manage times when certain issues must be completed by. An issue is often accompanied by a release, for example one issue we are working on right now is the Tim.JAR working prototype when we finshish we will create a release.

A realease is a snapshot of the code at a certain point in time, we use realeases as backups of our code so we always have a working version of the robot on hand.
