# Git Branch Orginization
*Rev 0.1-a*

------

## Branching

Definition: branches are the substance of code on a Git repository, they are where your code lives and dies, looking at it from above a branch is essentially a timeline of what has happened to your code,

In the tradition Github workflow, the master branch is your always ready to deploy branch, meaning the code in there should be hard and battle tested, Essentially a workable version of whatever your project is attempting to create. For us, this is less effective due to both the number of commiters we are working with and the fact that all of us are working in the same repository with no forks. The best way for us to get around this is to create Three primary branches that are upgraded with new commits from a feature branch to demonstrate.
____________________________________
![Alt Text](http://i.stack.imgur.com/ZVqYX.png)
___________________________________

This diagram shows off the three branches that we will be using,
  - Master: Essentially where all the final tested code will go this branch should be as bug-free as possible and well documented, essentially the code on a robot during a competition should be from this branch.
  - Hotfix: This branch should be used whenever  there is a major bug in master that we cant wait to go through the other two branches before we deploy it, normally we do a lot of this at a competition where we need to make fixes in the robot quickly.
  - Release: Our testing phase all code that is deemed "Ready-To-Test" should go here, not really a long term storage branch, though.
  - Develope: This is the busiest of the branches any normal change to the code should start off being branched away from this, and then worked on in a feature branch until it is ready to come back into this branch. Most of the time new features will be pushed up from here to Release right away, this branch exists so there is another layer of security between master and any possible broken features.
  - Feature: where all the meat is made, 80% of all commits will come out of these branches, with each "Feature Branch" focusing on one particular subject, "Feature", or Issue.

## Pulling

Definition: Pulling is the act of pulling code from a lower branch into a heigher one, this could also be called a merge, but merges are generlally only called then when coming down from a higher one into a lower.
