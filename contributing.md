
# Contributing Guide

1. Find a GitHub project you want to contribute to, and copy its HTTP/SSH link. For example, `https://github.com/leecccc/hyperbot.git`
2. Fork the project so you have your own copy.
2. On your computer, make a folder you want the project to be in and clone the project by running `git clone https://github.com/branden-akana/hyperbot` inside the folder.
3. *SWITCH TO THE `develop` BRANCH* if you already haven't: `git checkout develop`

## Workflow

Pull the latest changes from the upstream repository (the official one)
```bash
# gets all new commits from the upstream repository and merges it with your local copy
git pull upstream develop
```
*If you are working on a new feature*, branch off of `develop` into a new feature branch (name it whatever makes sense)
All your commits will go into the feature branch instead. Otherwise, you don't need to do this.
```bash
# switch to the develop branch
git checkout develop

# or switch to a new feature branch (that branches off of develop)
git checkout -b feature/somefeature develop
```
Work on the project as needed, and use the "add-commit" cycle
```bash
# edit some files
git add <file>
git commit -m "Work on feature/bug"
```
*If you were working on a feature* and it's complete, merge your feature branch into the develop branch.
```bash
# merges the feature branch into the develop branch
git merge feature/somefeature develop

# safely deletes the feature branch
git branch -d feature/somefeature
```
Pull changes from the upstream repository just in case changes were made to it while you were working
```bash
git pull upstream develop
```
Push your changes to the GitHub repository: (**make sure you are pushing to the correct branch**)
```bash
# push to the develop branch (on your fork)
git push origin develop

# push to a feature branch (if you aren't done yet)
git push origin feature/somefeature
```
