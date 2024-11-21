---
title: Useful Git Commands
tags:
  - terminal
  - ci
draft: false
---
This page is focused on providing and explaining the commands I most commonly use to deal with git via the terminal. I can only recommend everyone knowing at least the [[git#Basics|basic commands]] even if you use [[git#external tooling|external tooling]].

Even though external tools add an unnecessary amount of abstraction to your workplace and understanding, I can recommend them to use for [[git#visualization]].

## Basics

- normal workflow: implement your changes -> save file -> review changes via diff view -> stage files -> commit files -> publish the changes also to your remote

- initialize your project
  ```bash
  git init
  ```
- preparing a commit is called **staging**: it means you add files to the index that will be used for the next commit
- TODO: undo operation of git add -> git reset (???)
	```bash
	# adding a single file
	git add path/to/file
	
	# adding the files of a whole folder
	git add path/to/folder/
	
	# adding everything
	git add --all
	
	# or: add everything from the current directory
	git add .
	```
> [!Info]
>  Sometimes, git doesn't track a new file yet ... 
>  This also means that `git add --all` doesn't add it to the index.
> You have to explicitly add the folder or the file to the index.
	
- making a **commit**
	```bash
	# normal commit with message
	git commit -m "feat: your first commit"

	# commit while also adding all files
	# -> no need for an intermediate "add" step
	git commit -am "feat: adding all files automatically"	
	```
- **push** your changes: often you not only work alone but, want to synchronize your local repository with a remote repository (e.g., Github) to enable collaboration
	```bash
	# publish your changes to the default origin
	git push
	
	# don't do this unless you want to make your colleges hate you
	git push --force	
	```

## Helpers

> [!tip] output the current state of your git repository
> this command gives you information about which files you have not versioned yet, changed or staged
>
> ```bash
> git status
> ```

- git history

  ```bash
  git log
  ```

- visualizing the current changes

  ```bash
  # for unstaged files
  git diff

  # for staged files
  git diff --cached
  ```

## Merging

git checkout main utils/arc_utils.py to reset a file

## Branching

## Working with remote
- TODO: git clone
- TODO: git upstream einrichten
- pull changes: synchronize your local repository with incoming changes from the remote repository
	- be careful: merge conflicts can already happen here
	- no local changes and want to pull the newest changes
	```bash
	# just update the information you have about the remote repository 
	# without actually updating your files (nothing happens)
	git fetch

	# update to your local files with changes from remote
	git pull

	# goated command
	git pull --rebase --autostash 
	```
	- TODO:
	- explain the problems that might occur here -> merge conflicts
	- conflicts with un-commited changes
	
## Fixing mistakes

## Advanced
- TODO: git reset hard and soft
- 

### Submodules
_on your own ..._

## External Tooling

### Visualization
