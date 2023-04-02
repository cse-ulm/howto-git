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

## Basic Commands
Once you have a Git repository set up, you can start using some basic commands to manage your files and track changes. Here are some of the most common Git commands you'll need to know:

### [git status](https://git-scm.com/docs/git-status)

The git status command shows you the current state of your repository, including which files are staged (ready to be committed) and which files have been modified but not yet staged. 
Create a new file `README.md` in the repository.
To see the current status of the repository, run `git status`.
You should see the following output:
```bash
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)
```
This output tells us that we're on the `main` branch, there are no commits yet, and there's a new file called `README.md` that's untracked.

### [git add](https://git-scm.com/docs/git-add)
The git add command is used to stage changes to your repository. You can add specific files or directories by name.

To start tracking changes to the `README.md` file, we need to add it to the staging area. Run the following command:
```bash
git add README.md
```
Now if we run `git status` again, we should see the following output:
```bash
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md
```
This output tells us that we've added the README.md file to the staging area, and it's ready to be committed.

With `git add .` you can stage all files in the directory.

### [git commit](https://git-scm.com/docs/git-commit)
To commit the changes, run the following command:
```bash
git commit -m "Add README.md file"
```
This will create a new commit with the message "Add README.md file".

Now if we run `git status` again, we should see the following output:
```bash
On branch main
nothing to commit, working tree clean
```
This output tells us that there are no changes to commit, and the working directory is clean.

### [git diff](https://git-scm.com/docs/git-diff)
The `git diff` command shows the differences between the current state of your files and the most recent commit. Let's make some changes to the `README.md` file and then use `git diff` to see the differences.

Open the README.md file and add the following line at the end of the file: `This is a new line in the README file`.
Save the file and then run `git diff README.md`.

This will show you the differences between the README.md file in the working directory and the version in the staging area. You should see output similar to the following:

```bash
diff --git a/README.md b/README.md
index e69de29..1154593 100644
--- a/README.md
+++ b/README.md
@@ -0,0 +1 @@
+This is a new line in the README file
```
This output shows that we added a new line to the `README.md` file. The lines with a `-` indicate lines that were removed, and the lines with a `+` indicate lines that were added.

### [git pull](https://git-scm.com/docs/git-pull)
The `git pull` command is used to fetch and merge changes from a remote repository. It is often used when collaborating with others on a project.

For example, if you're working on the main branch and want to pull changes from the origin remote repository, run the following command:
```bash
git pull origin main
```

### [git push](https://git-scm.com/docs/git-push)
The `git push` command is used to push your changes to a remote repository. This is typically used when you want to share your changes with others or backup your work.

For example, if you're working on the main branch and want to push your changes to the origin remote repository, run the following command:
```bash
git push origin main
```

### [git fetch](https://git-scm.com/docs/git-fetch)
The `git fetch`  command is used to download any changes that have been made to a remote repository and store them in your local repository. However, unlike the `git pull` command, git fetch only downloads the changes and does not automatically merge them into your local branch. This means that after running `git fetch`, you will have the updated changes available in your local repository, but you will need to manually merge them into your local branch if you want to apply them.

You can use `git fetch` before you start working on your local branch to ensure that you have the latest changes from the remote repository. By doing this, you can avoid conflicts that may arise if someone else has made changes to the same files you're working on.

## Branching and Merging

### Creating a new branch

### Switching between branches

### Merging branches

### Resolving merge conflicts

## Advanced Commands

### git log

### git reset

### git revert

### git stash

## Best Practices

### Writing good commit messages

### Using branching effectively

### Keeping your repository clean
