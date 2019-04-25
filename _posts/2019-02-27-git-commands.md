---
layout: post
title: git commands
date: 2019-02-27
summary: ""
categories: git
---

![desk](../../../../../images/git-flow.jpg)

## stash

#### stash the changes:

<code>git stash</code>

#### lists stashs:

<code>git stash list</code>

#### apply the latest stash:

<code>git stash apply</code>

#### apply a specific stash:

<code>git stash apply stash@{number}</code>

#### remove a specific stash from the stash list:

<code>git stash drop stash@{number}</code>

#### apply and remove from the stash list:

<code>git stash pop stash@{number}</code>

## remote

#### add a remote:

<code>git remote add remote-name remote-url</code>

#### lists remotes:

<code>git remote -v</code>

#### rename a remote:

<code>git remote rename old-name new-name</code>

#### remove a remote:

<code>git remote remove remote-name</code>

## push

#### push into remote:

<code>git push remote-name branch-name</code>

#### heroku: push any branch into master and start a new deploy:

<code>git push heroku-remote-name branch-name:master</code>

## branch

#### lists branches:

<code>git branch</code>

#### checkout and create a new branch from the working directory:

<code>git checkout -b branch-name</code>

#### create a new branch:

<code>git branch branch-name</code>

#### deletes a branch in safe mode (prevents deleting branchs with unmerged changes):

<code>git branch -d branch-name</code>

#### deletes a branch in force mode:

<code>git branch -D branch-name</code>

#### rename the current branch:

<code>git branch -m new-branch-name</code>

#### lists all remote branches:

<code>git branch -a</code>

---

useful links:
* [git command explorer](https://gitexplorer.com/);

* [git cheat sheet](http://files.zeroturnaround.com/pdf/zt_git_cheat_sheet.pdf);

* [github - folha de dicas de git](https://services.github.com/on-demand/downloads/pt_BR/github-git-cheat-sheet.pdf).

---