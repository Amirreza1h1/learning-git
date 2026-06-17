# Learning-git
---
Hi everyone,

I am learning Git from W3Schools and created this repository as a short cheat sheet.
The goal is to share simple Git concepts with very short command examples.

If this repository helps you, feel free to star it and share it with others.

## Introduction
---

<p>This repo is useful for beginner to intermediate programmers who want a quick summary of Git.
I started it for myself while learning Git, then decided to share it with others.</p>
<p>This is not a full Git course. It is a short reference for common Git concepts and commands. If there is a problem or confusion, you can check www.w3school.com for more examples and details or ask me.</p>

<p>I decided to organize the topics in my own order instead of following the exact same order as W3Schools.</p>

## Before You Start
<p>This repo does not explain how to install Git or create a remote account on GitHub, GitLab, or other platforms.

After installing Git, it is important to set your name and email address correctly because Git uses them to identify your work.

You can check your current global Git name and email with:</p>

```bash
git config --global user.name
git config --global user.email
```

<p>Before starting the concepts, it is helpful to know that Git works with different places for files: local repository, staging area, stash, and remote repository.</p>

## Basic concepts

### Git Repository

A Git repository is a project folder that Git tracks.
When you create a repository, Git can start saving the history of your files.
```bash
git init    #Create a new Git repository
git status  #Check the repository status
```

### Git Status

`git status` shows the current state of your project. It tells you which files are changed, staged, untracked, or ready to commit.

```bash
git status
git status --short
```

### New Files and Staging Area

When you create a new file in a Git repository, Git can see it as an untracked file. You need to add it to the staging area before committing it.
The staging area is where you prepare files before saving them in a commit. You can stage one file or all changed files.

```bash
git status
git add file-name
git add .   #add every changed file
```
### Commit

A commit saves your staged changes in the repository history. A good commit message should be short and clear.

```bash
git commit -m "Add homepage"
```
### Commit History

Git history shows the commits that were saved in the repository. It helps you review what changed and when it changed.

```bash
git log
git log --oneline
```

### Branch

A branch lets you work on a separate version of your project. It is useful when you want to add or test something without changing the main branch directly. We usually use it to add a feature or when we want to release a new version of the project.

```bash
git branch feature-navbar   #create branch
git switch feature-navbar   #if there is no such a branch, create and switch
git checkout -b feature-navbar  #create and switch
```
If branch does not exist, checkout alone will not create it. So for a beginner is better to use checkout instead of switch.

### Merge

Merge combines changes from one branch into another branch. Usually, you switch to the target branch first, then merge the other branch into it.

```bash
git checkout main
git merge feature-navbar
```

### Tag

A tag is a name for a specific commit. Tags are often used for versions, such as releases.

```bash
git tag v1.0.0
git tag
```

### Stash

Stash temporarily saves your unfinished changes. It is useful when you need to switch branches but are not ready to commit.

```bash
git stash
git stash pop
```
### Help

Git help shows information about Git commands. It is useful when you forget how a command works.

```bash
git help status
git status --help
```

### Basic Workflow

A basic Git workflow is checking your files, staging changes, committing them, and reviewing the result. This is the common cycle for saving work locally.

```bash
git status
git add .
git commit -m "Update files"
git log --oneline
```

### Best Practices

Good Git habits make your project easier to understand. Use clear commit messages, commit related changes together, and check status often.

```bash
git status
git commit -m "Fix navigation links"
```

### Glossary

A glossary is a short list of important Git words. It helps beginners remember terms like repository, commit, branch, merge, stage, and remote.

```bash
git help glossary
```

## Advanced concepts
---


### .gitignore

`.gitignore` tells Git which files or folders it should not track. It is useful for secret files, temporary files, dependencies, and generated files.

```bash
touch .gitignore
git status
```

Example `.gitignore` content:

```gitignore
node_modules/
.env
```
### GitHub / Remote Repository

A remote repository is a version of your project stored online, such as on GitHub. It helps you back up your project and share it with others.

```bash
git remote -v
git remote add origin https://github.com/user/repo.git
```


## Resources