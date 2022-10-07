# Git commands

![GIT](git.png)
[Documentation](https://git-scm.com)

## Username & Email configuration

### First time use you should enter following commands:

* `git config --global user.name "John Doe"` - with your username instead of "John Doe"

* `git config --global user.email johndoe@example.com`  - with your email instead of "johndoe@example.com"

## Repo initialization 

`git init` - initialization of local repo

## Basic commands

`git help` - shows common git commands with description

`git status` - information about current git state

`git log` - shows commit history

`git log --oneline` - shows commit history, each commit on single line with shortcut hash

`git checkout` - moving between commits

`git checkout HEAD^` - moving one commit back from HEAD

   * `git checkout <commit_hash>^` - moving one commit back from certain commit

   * `git checkout <branch_name>^` - moving one commit back from last commit of branch_name

`git checkout HEAD~<num>` - moving \<num\> commits back from HEAD

   * `git checkout <commit_hash>~<num>` - moving \<num\> commits back from certain commit

   * `git checkout <branch_name>~<num>` - moving \<num\> commits back  from last commit of branch_name

`git checkout master`  - returns to actual state

`git diff` - shows difference between current file and its committed version

`git rebase <dest_branch>` - copies commits of current branch and moves them to dest_branch


### Commiting

 1. `git add <filename>` - to begin tracking new file or to stage changes in a file, that was already tracked

    * `git add -A` / `git add . `- to track or stage all files in repo

 2. `git commit -m "some message"` - to create commit record

    * `git commit -am "some message"` - stage & commit (only for files already being tracked)

### Undoing things

`git reset <commit_hash>` - returns repo on current commit state, like if latest commits never existed

`git revert <commit_hash>` - makes new commit with changes opposite to changes made in latest commit

`git commit --amend` - rewrites last commit with new changes (changes should be staged before)

`git reset HEAD <file>` / `git restore --staged <file>` - unstages file staged file

`git checkout -- <file>` / `git restore <file>` - discard changes in file ( **Any local changes you made to that file are gone** )

 ### Branching

 `git branch` - shows all branches

 `git branch <branch_name>` - create new branch

 `git checkout <branch_name>` - switch to branch branch_name

 `git branch -d <branch_name>` - delete branch branch_name

 `git branch -D <branch_name>` -  delete branch branch_name forced

 `git checkout -b <branch_name>` - creates new branch branch_name and switches to it

 `git merge <branch_name>` - merges changes from branch_name to current branch

 `git branch --move bad-branch-name corrected-branch-name` - rename branch

 `git branch -f <branch_name> <commit_hash>` - moves branch to certain commit forced

### Work with remote repo

`git clone <url>` - clone repo from url

`git pull` - pulls changes from remote repo

`git push` - pushes changes to remote repo