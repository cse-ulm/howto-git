# howto-git

## Introduction
Git is a powerful tool for managing and tracking changes in your code. It allows you to collaborate with others and easily revert to previous versions of your code if necessary. In this tutorial, we will cover the most important Git commands and workflows, so you can start using Git in your own projects.

## Setting up Git

Before you can start using Git, you need to install it on your computer and configure it with your name and email address. Here's how to do it:

### Installing Git
If you don't already have Git installed on your computer, you can [download](https://git-scm.com/downloads) it from the Git website. Follow the instructions for your operating system to install Git.

Once you've installed Git, you can check the version by opening a terminal window and running the command:
```bash
git --version
```
If you see a version number printed to the console, you've successfully installed Git!
### Configuring Git
Once you have Git installed, you need to configure it with your name and email address. Open a terminal or command prompt and run the following commands, replacing "Your Name" and "you@example.com" with your own information:

```bash
git config --global user.name "Your Name"
git config --global user.email you@example.com
```
These commands will set your name and email address as the default identity for all of your Git commits. You only need to run these commands once, and Git will remember your settings.

That's it! You're now ready to start using Git.

## Creating a Repository
A Git repository is a collection of files and directories that are managed by Git. You can create a new repository for your project using the git init command.

### [git init](https://git-scm.com/docs/git-init) - Creating a New Repository
Create a new repository by navigating to the directory where you want to store your project and run the following command:

```bash
git init
```
This will initialize a new Git repository in the current directory. Git will create a hidden .git directory to store all the repository's metadata.

### [git clone](https://git-scm.com/docs/git-clone) - Cloning an Existing Repository
If you want to work on an existing Git repository, you can clone it to your local machine using the git clone command. For example, to clone a repository from GitHub, you can run the following command:

```bash
git clone https://github.com/username/repository.git
```
This will create a new directory with the same name as the repository and clone all the files and directories from the remote repository.

That's it! You now have a Git repository that you can use to manage your project's code.

## Basics
### - git status 

### - git add

### - git commit

### - git pull

### - git push 

### - git fetch

## Branches

### - git switch

## Best practices 

### - git rebase

