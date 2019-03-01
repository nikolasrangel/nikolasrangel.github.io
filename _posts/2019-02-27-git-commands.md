---
layout: post
title: git commands
date: 2019-02-27
summary: ""
categories: git
---

![desk](../../../../../images/git-flow.jpg)

## stash

#### coloca na pilha:

<code>git stash</code>

#### lista os stashes da pilha:

<code>git stash list</code>

#### aplica o stash mais recente da pilha:

<code>git stash apply</code>

#### aplica o stash especificado:

<code>git stash apply stash@{number}</code>

#### remove da pilha o stash:

<code>git stash drop stash@{number}</code>

#### aplica e remove da pilha o stash:

<code>git stash pop stash@{number}</code>

## remote

#### adiciona remote:

<code>git remote add remote-name remote-url</code>

#### lista remotes:

<code>git remote -v</code>

#### renomeia remote:

<code>git remote rename old name</code>

#### remove remote:

<code>git remote remove remote-name</code>

## push

#### push para remote:

<code>git push remote-name branch-name</code>

#### heroku: push de branch para a master:

<code>git push heroku-remote-name branch-name:master</code>

## branch

#### lista branches:

<code>git branch</code>

#### cria branch e muda para ela:

<code>git checkout -b branch-name</code>

#### apenas cria uma branch:

<code>git branch branch-name</code>

#### deletes a branch in safe mode (prevents deleting branchs with unmerged changes):

<code>git branch -d branch-name</code>

#### deleta branch forçando:

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