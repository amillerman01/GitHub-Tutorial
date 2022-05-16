# GitHub Tutorial  <!-- omit in toc -->

For all your git learning needs. This tutorial will focus how to interact with the cloud based version control system known as [GitHub](https://github.com/), using [GitHub Desktop](https://desktop.github.com/) to do so.

## Before beginning <!-- omit in toc -->

You will need an account on [GitHub](https://github.com) in order to participate in this workshop. If you sign up using your school email, you can potentially get a free upgrade to a [pro](https://docs.github.com/en/get-started/learning-about-github/githubs-products#github-pro) account. You can always change the email on your account later to reclaim your account for yourself once you've graduated. If you're interested in getting a free pro account using your school email address, you can find more information [here](https://education.github.com/pack).

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
  - [2.9. Cleaning out sensitive file data](#29-cleaning-out-sensitive-file-data)
- [3. Glossary of terms](#3-glossary-of-terms)
  - [3.1. Repository](#31-repository)
  - [3.2. Commit](#32-commit)

# 1. The Basics

## 1.1. What is Github?

GiHub is a user friendly, cloud based version control system. With a GitHub account, you can make [repositories](#repository) to store your source code, keep track of your changes make to your code (known as [commits](#commit)), and access the entire commit history of each and every file you add to a repository. You can keep track of multiple projects, generally having them all logically separated into their own repositories, and each of them will keep track of their own file history. 

At its most basic level, GitHub gives you the tools to:
- Save your code to a cloud server, allowing you can access it and update it from anywhere
- Consolidate your code to a single location, called a repository, so you never lose it or wonder where the most current version of the code is on your computer
- Track changes you make to your code, giving you the ability to easily recover old copies of your code if you need to
- Discard changes to your code before committing it to GitHub, for when your current code changes are completely broken
- Collaborate with others on the same codebase without having to continuously send each other individual files to be manually updated
- Help make sure nobody's code changes are lost when you're collaborating on a project together, especially when multiple people are working on the same files at the same time

You can find more info [here](https://kinsta.com/knowledgebase/what-is-github/).

## 1.2. What you'll need to get started

There are many ways you can interact with your GitHub repositories, including through the terminal, through your code editor, or using a separate GUI program. In this tutorial, we're going to focus on that last option, in the form of [GitHub Desktop](https://desktop.github.com/). Visit that link and download the program for your computers operating system.

When you install GitHub Desktop, it will also install the latest version of Git along with it. [Git](https://git-scm.com/) is the underlying open-source technology behind services like GitHub, providing us the version control system functionality.

Once you've installed GitHub Desktop, you'll need to [connect your github account to it](https://docs.github.com/en/desktop/installing-and-configuring-github-desktop/installing-and-authenticating-to-github-desktop/authenticating-to-github#authenticating-an-account-on-github-1). Note that if you're working on a public machine, you need to make sure you log out of the program to disconnect your account from the program.

## 1.3. Making your first repository

You can make repositories either directly on github.com or in the GitHub Desktop program. We're going to go through the process using GitHub Desktop, which you can find the steps for [here](https://docs.github.com/en/desktop/installing-and-configuring-github-desktop/overview/creating-your-first-repository-using-github-desktop).

It's important to note that once you make a repository on your computer (or [clone one](#14-cloning-your-repository)), GitHub Desktop is essentially watching for changes you make to any files inside of the folder that contains your repository. It knows to watch for changes in this folder because of a hidden item called the .git folder. Any files you add, change or remove will be determined to be changes to the repository. What you do with those changes is something discussed in the [Making your first Commit](#16-making-your-first-commit) section.

For more info, see the official documentation from GitHub [here](https://docs.github.com/en/get-started/quickstart/create-a-repo), or documentation on doing it specifically through GitHub Desktop [here](https://docs.github.com/en/desktop/installing-and-configuring-github-desktop/overview/creating-your-first-repository-using-github-desktop)

## 1.4. Cloning your repository

If you want to work on a repository on your computer that you didn't create from your computer, you need to clone that repository. Cloning allows you to make a local copy of the repository on your computer (we'll talk about local copies of repositories in the next section). Once you have a local copy on your computer, you can change the code on your local copy, and as long as you have permissions set on the repository you can publish your changes up to the repository on github itself.

You can find the steps to clone a repository to GitHub Desktop [here](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/adding-and-cloning-repositories/cloning-and-forking-repositories-from-github-desktop#cloning-a-repository).


## 1.5. Local vs origin

When you're working with your GitHub repository code on your computer, there are always at least 2 copies of that repository: One is the copy on the GitHub servers themselves, on the cloud (known as **origin** or remote). The other copy is the local repository on your computer. 

When you make changes (aka **commits**) to your code using GitHub Desktop, you are updating the local repository code. Those changes will not make it to the remote copy of the repository until you **push** those changes to origin. That means that if you are collaborating with someone on a repository, they will not be able to receive your changes to the code until you push that code up. Once you do push the code, it will be sent to the GitHub servers, and you'll be able to see the changes on your repository on [github.com](https://github.com).

For more info, see the official documentation from Git [here](https://git-scm.com/book/en/v2/Git-Branching-Remote-Branches).

## 1.6. Making your first commit

Once you've got your repository setup on your computer, your local repository is now watching for any changes you make to any files inside of the repository folder (i.e. the folder that contains the .git hidden folder inside of it). 

Once you make changes to a file, GitHub Desktop will display those changes on the left hand side, indicating whether it's a new file, a change to a file, or if the file has been deleted. These are different types of changes that GitHub wants to track once you commit them. Each change is tracked on the history of each individual file.

These changes are not part of your local repository history, until you have committed them. They are pending, waiting to be committed to the repository. In order to commit your changes, you must select the files you want to include in the commit (all the files that have changed are selected by default), add a commit summary message that indicates what changes were made to the repository, optionally add a description to go into further detail about what changes were made, and then click on the commit button. This will add the changes to the history of the respository, solidifying those changes as part of the official changes tracked on the respository.

Committing your changes only updates the local copy of your repository. It does not update the code on GitHub's servers. In order for your committed changes to be added to GitHub's servers, you must push the changes.

For more info, see the official documentation from GitHub on how to make a commit using GitHub Desktop [here](https://docs.github.com/en/desktop/installing-and-configuring-github-desktop/overview/creating-your-first-repository-using-github-desktop#part-5-making-committing-and-pushing-changes) and [here](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/making-changes-in-a-branch/committing-and-reviewing-changes-to-your-project).

## 1.7. Fetch, push and pull

Since there are two copies of the repository that you're interacting with (the local copy and the remote copy on github.com), you need to make sure that your local updates are making it to the remote server, and you also need to make sure that you are receiving the updates from the remote server to your local copy of the repository. That's where fetch, push and pull come in. 

Fetch is a the command you use to check if the remote server has any changes for you.

Pull is a the command you use to retrieve those changes from the remote server and **pull** them down onto your computer.

[Push](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/making-changes-in-a-branch/pushing-changes-to-github#pushing-changes-to-github) is a command you use to send your changes from your local repository up to the GitHub servers.

For more info on fetching and pulling, see the official documentation from GitHub [here](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/keeping-your-local-repository-in-sync-with-github/syncing-your-branch#pulling-to-your-local-branch-from-the-remote).

## 1.8. Browsing the commit history

Every commit you make to your repository is adding to the history timeline of the repository. You can view this history directly in [GitHub Desktop](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/making-changes-in-a-branch/viewing-the-branch-history) or you can view it on github.com. Each item listed in the history is a commit that someone made to the repository, and will show you all the files changed due to that commit at that time. This gives you a nice way to view code changes you've made to any individual file, so you can always retrieve old versions of code if you need it.

You can also revert commits from the history, to undo changes to the repository code, outlined [here](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/managing-commits/reverting-a-commit).

For more info, see the official documentation from GitHub [here](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/making-changes-in-a-branch/viewing-the-branch-history).

## 1.9. Making and publishing branches

One of the other very useful aspects of using a version control system is the ability to maintain multiple versions of the code at the same time. Oftentimes you need to maintain at least two copies of your code:

- A stable copy of the code, usually referred to as the production copy of the code
- A development copy of the code where you are building new features, fixing bugs and testing everything new before moving the code into production

In order to maintain multiple copies of the code in a repository, you need to create separate branches of the code. A branch is essentially a copy of the repository code and its history. Commits you make to a branch will not be visible on other branches.

By default, your repository comes with a single branch: the main branch. You can make a new branch off of the main branch, as outlined [here](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/making-changes-in-a-branch/managing-branches#creating-a-branch).

Just like when you commit code to your repository, creating a branch on your local copy of the repository does not add the branch to the GitHub servers by default. In order for your new branch to be available on github.com, you must [publish your branch](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/making-changes-in-a-branch/managing-branches#publishing-a-branch).

## 1.10. Switching Branches

Once you've made a new branch, and added commits to it, you will eventually want to switch back to the main branch (or another feature branch). In order to switch branches, you can follow the steps outlined [here](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/making-changes-in-a-branch/managing-branches#switching-between-branches).

# 2. Extra Items

## 2.1. Making commits directly on github.com

You can make changes directly to your repository from the github.com website. This automatically makes changes to the remote copy of the repository, instead of your local copy. In order to see those changes on your computer, you will need to fetch and pull the changes down.

Editing files on github.com is useful for small changes and updates, but is not as viable when you are trying to add multiple files or changes at once, especially in complex folder structures. That is a task better suited for being done locally on your computer and pushed to the GitHub serveers.

For more info, see the official documentation from GitHub [here](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files).

## 2.2. Inviting people to collaborate

Once you've created a repository, you can invite other github users to collaborate with you on your repository. Collaborators can be given various different permission levels, based on the roles they are going to play in your repository. The steps to invite collaborators to your repository can be found [here](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-user-account/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository).

Users who are invited to collaborate on a repository will need to access their email and accept the invite they receive there.

## 2.3. .gitignore file

Sometimes there are files we don't want GitHub to track on the repository, such as automatically generated files when you compile your code, large library files that are added via tools like npm (see [npm packages and modules](https://docs.npmjs.com/about-packages-and-modules)), or files that contain information such as security tokens and passwords. These files are important to run your application locally, but we need a way to ignore them when we are making commits to our repository. 

We can do this by creating a `.gitignore` file. Once you create this text file, you can add file and folder names to it that you don't want to be added to your GitHub repository, even though they're in the folder that GitHub Desktop is watching for changes. You can fine more information on how to use the `.gitignore` file [here](https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files).


## 2.4. Repository settings

Here they can change privacy levels, archive repository, delete repository, etc.

For more info, see the official documentation from GitHub [here]().

## 2.5. Creating pull requests

Pull requests are ways you can create comparisons between branches 
- Show what a pull request is and how it works
- potentially use this for assignments, where they submit pull requests (optional idea)

For more info, see the official documentation from GitHub [here]().

## 2.6. Deployment

- Pending my own notes. Until then, you can see the documentation directly from GitHub [here](https://docs.github.com/en/rest/deployments/deployments)

## 2.7. GitBash

- `git clean -fdx` to clear out folders that don't belong anymore

- Pending my own notes. Until then, you can see the documentation directly from GitHub [here](https://docs.github.com/en/rest/deployments/deployments)

## 2.8. Github and VSCode

- Pending my own notes. Until then, you can see the documentation directly from GitHub [here](https://docs.github.com/en/rest/deployments/deployments)


## 2.9. Cleaning out sensitive file data

- Can be done using a tool found [here](https://github.com/rtyley/bfg-repo-cleaner)

# 3. Glossary of terms

## 3.1. Repository

A repository is logical grouping of source code, usually centered around a specific project or solution. You can find more info [here](https://docs.github.com/en/repositories/creating-and-managing-repositories/about-repositories)

## 3.2. Commit

- Pending my own notes. Until then, you can see the documentation directly from GitHub [here](https://docs.github.com/en/rest/deployments/deployments)
