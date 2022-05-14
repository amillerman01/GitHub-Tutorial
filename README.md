# GitHub Tutorial  <!-- omit in toc -->
For all your github learning needs

## Before beginning <!-- omit in toc -->

- Be sure to mention relevent experience you have with github in industry, highlighting the important of using a version control software throughout, giving reasons why each part is useful and how in day to day work as a developer.

- [1. The Basics](#1-the-basics)
  - [1.1. What is Github?](#11-what-is-github)
  - [1.2. What you'll need to get started](#12-what-youll-need-to-get-started)
  - [1.3. Making your first repository](#13-making-your-first-repository)
  - [1.4. Cloning your repository](#14-cloning-your-repository)
  - [1.5. Local vs origin](#15-local-vs-origin)
  - [1.6. Making your first commit](#16-making-your-first-commit)
  - [1.7. Fetch, push and pull](#17-fetch-push-and-pull)
  - [1.8. Browsing the commit history](#18-browsing-the-commit-history)
  - [1.9. Making and publishing branches](#19-making-and-publishing-branches)
  - [1.10. Switching Branches](#110-switching-branches)
- [2. Extra Items](#2-extra-items)
  - [2.1. Making commits directly on github.com](#21-making-commits-directly-on-githubcom)
  - [2.2. Inviting people to collaborate](#22-inviting-people-to-collaborate)
  - [2.3. .gitignore file](#23-gitignore-file)
  - [2.4. Repository settings](#24-repository-settings)
  - [2.5. Creating pull requests](#25-creating-pull-requests)
  - [2.6. Deployment](#26-deployment)
  - [2.7. GitBash](#27-gitbash)
  - [2.8. Github and VSCode](#28-github-and-vscode)

# 1. The Basics

## 1.1. What is Github?

- version control system
- saves your stuff and tracks changes you make
- protects you from losing code
- helps make code collaboration easier
- central place to store and retrieve code projects
- great thing to have on your resume

## 1.2. What you'll need to get started

- Make a github account on github.com
  - Use your school email for a free pro account
- install git
  - might need to be on a usb stick in the labs
- install github desktop
  - Machines should install it on their machines soon after they login
  - login to github desktop
- optionally use gitbash instead

## 1.3. Making your first repository

- Make it on github.com
- Name it something relevant to class like WEB315S22
- set it as private initially
- add a readme.md by default
- ignore license

## 1.4. Cloning your repository

- go to file - settings
- login (will open browser and login that way)
- Click clone repository
- Find your repository on the list
- Choose folder it should go into
- After cloning, view it in file explorer to see it locally on the machine
  - need them to understand that changes made to files in this folder will show up as pending changes to github

## 1.5. Local vs origin

- Explain difference between local repository and remote repository (origin)

## 1.6. Making your first commit

- make changes to readme file
- show that they are pending until you commit them
- commit changes locally, setting a relevant name for the summary
- description optional for now
- emphasize that commit didn't make it to github.com yet because we didn't push
  - changes can't be marked unless they are PUSHED
## 1.7. Fetch, push and pull

- Push change so it's on github now
- View on github to see changes
- potentially make changes to file on github so you can then fetch on github desktop and pull changes

## 1.8. Browsing the commit history

- make a few more commits and then view history on github desktop and github.com
- draw attention to time stamps, files changes, different views for commit history on github.com, etc
- also emphasize that code is never lost, you can always recover things in the github commit history
- you can also undo commits based on the commit history
  - show how through github desktop

## 1.9. Making and publishing branches

- Make a branch off main
- Make commits and push them, to show it doens't affect main branch
- change branches on github.com to show where changes exist

## 1.10. Switching Branches

- Show how to switch branches locally on github desktop
- Show what happens when you switch branches with pending changes 
  - stash changes vs bring them with you
- Higlight that your local copy of the repo only contains the copy of the files based on the current branch that is checked out
- make sure they understand that making a branch is based on the branch you're currently in, or main, depending on what branch you're currently in

---

# 2. Extra Items

## 2.1. Making commits directly on github.com

- Higlight the idea of being able to make commits directly on website
- make sure they understand that they can't easily make folders there
  - uploading complex project code should be done in github desktop
  - minor tweaks can be done on github.com directly
- show file histories

## 2.2. Inviting people to collaborate

- have them invite you to their repository, so you can view it
  - private repos protect them from potential academic integrity issues coming up later
  - You need to accept invites once they invite you, can be done later
- Discuss permission possibilities and how awesome it is that you can invite collaborators for projects in industry

## 2.3. .gitignore file

- Important file to make only the files you want are added to your repository
- Minimizes how many files get pushed to github, especially external libraries and files generated when executing your 

## 2.4. Repository settings

- Here they can change privacy levels, archive repository, delete repository, etc.

## 2.5. Creating pull requests

- Show what a pull request is and how it works
- potentially use this for assignments, where they submit pull requests (optional idea)

## 2.6. Deployment

- tbd

## 2.7. GitBash

- tbd
- `git clean -fdx` to clear out folders that don't belong anymore

## 2.8. Github and VSCode

- tbd
