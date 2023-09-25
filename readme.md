# Instructions for Git

* git clone url.com // to clone the repository
* cd into the folder you have cloned
* git status // to see the status of our folder
* git add readme.md
* git status
* git commit -m "Readme file updated"
* git remote add origin https://github.com/JRC404/test-app.git // because we cloned the repository, we don't need the origin, but  it is a needed step if you do not clone
* git push -u origin main

## Extra Comments

* 'git add' can have multiple endings:
    * git add readme.md
        * This will add a single file to the staging area
    * git add readme.md index.ts
        * This will add two files to the staging area
    * git add .
        * This will add all changed files to the staging area
    * git add *
        * This will add all changes in the current directory but not the sub directory
    * git add -all OR git add -A
        * This will add hidden files but try not to add hidden files. They are often hidden for a reason. .gitignore is an exception
        
# VS Demonstration
* Using the 'git changes' window, we can use a GUI instead of a command line interface for Git commits
* If you don't see 'git changes' - click 'View' and then 'git changes'

# VS Code Demonstration
* On the left hand side, you will see a tree with 3 circles, that is our git GUI tool
* That will show you the changes that have been made in the application
* At this moment in time, I have 1 change:
    * readme.md
* To commit the change, I have to do 3 things:
    * Type a message for Git to highlight what has been changed: 'readme updated with VS Code Instructions'
    * I need to stage the commit by clicking the + icon next to the 'Changes' heading
    * Click the dropdown arrow next to 'Commit' and select 'Commit & Push'

## Version Numbers of Applications

* 1.0.0
* The far right 0.0.1 <- Is a minor change to the applcation
    * 0.0.2 <- A minor change from 0.0.1
* The middle number 0.1.0 <- is a bigger change but not a drastic move
* The first number 2.0.0 <- is a major release of an application / programme / software tool
* https://support.apple.com/en-gb/HT213407#1601 for reference

## Branching

* We can use brnaching to allow engineers to try different solutions without causing issues on the main codebase

```
git branch example
git checkout example
```

* To merge with main, we need to do the following:
```
git checkout main
git pull origin main // to get the latest from main
git merge example
git push origin main
```

* Sometimes, we don't need to keep the test branch alive, so we can delete the branch:
```
git branch -d example
git branch -D example // this will force the branch to delete even if there are unmerged changes
```