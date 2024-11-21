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

## Fixing mistakes

## Advanced

### Submodules

## External Tooling

### Visualization
