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

### New Files

When you create a new file in a Git repository, Git can see it as an untracked file. You need to add it to the staging area before committing it.

```bash
git status
git add file-name
git add .   #add every changed file
```

## Advanced concepts
---
### .gitignore
<p>In real projects for managing security, we don't want to address some of our assets, keys, passwords and other type of secret files.</p>
<p>On one hand, we can move our secret things out of the project folder and use absolute or relative path to use them. On the other hand, with changing of some modules' built-in properties as an essential accessible core, manner and workflow of our connections come into a serious problem.</p>
<p>In that case, we use <b><i>.gitignore</i></b> file to tell git not to track the changes or content of it.</p>

<p>How to use it will be here soon.</p>

## Resources