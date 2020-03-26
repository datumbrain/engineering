---
layout: post
title: Commit Messages
author: Fahad Siddiqui
authorUrl: https://github.com/fahadsiddiqui
date: "2020-03-26 05:43:49"
---

![](/assets/commit-post-image.png)

Formatting commit messages and writing a proper description that reflects the code done can be tiresome. But are an essential part of a growing project. When more than one developers are working on the same code-base as you are, you will experience a lot of back and forth happening. A lot of code getting dumped, some of it reverted, some of it staying in the pull/merge requests for a while.

In distributed teams, this may happen due to not following the same pattern. Conventions are subjective, always. But you can try to bring things, at least, to a common ground where everyone agrees upon it.

Here are a few good examples what _Datum Brain_ follows to format a commit message.

# Task ID

There is a task ID assigned to each task attempted. We do it normally through Trello for some projects (by using _Card Numbers_ power-up by _Reenhanced_) and using Atlassian's Jira for some of the other projects. Task IDs consist of two parts separated by a hyphen.

Assuming we have a task in a project named "My Good Project", it will be assigned a three-letter code (by convention) followed by a hyphen and a task number. Such as, `MGP-1`.

`MGP-1` will be prepended with commit message wrapped in square brackets as

```
[MGP-1]
```

# Title Line

Commits can be too long or too short, depending on the work done in code against that commit. A commit message may have or may not have the description if it's not that much of a work.

Commit title line should always be a summarised information lesser than 50 characters.

## Why 50 Characters?

50 characters is limit of characters some git applications have on their default zoom-ed page view. So it is better to keep it short to 50 characters rather seeing ellipses that cut off the title.

Let's assume `MGP-1` was about adding a few lines in `.gitignore` file.

It is not that much of a work, so may be, we can represent it in one title line without a body.

## Bad Examples

> "Frustrated at 2AM."

```
done
```

> "Too fast, trying out something that might work."

```
smthing
```

> "Stubborn as hell."

```
[mgp-1]ds store added in git ignore
```

> "Won't follow the system. Rebellion."

```
[MgP-1] adding `.DS_Store` in .gitignore  file
```

## Good Examples

> "Contributing to the code."

```
[MGP-1] Adding `.DS_Store` in .gitignore File
```

> "Playing my part."

```
[MGP-1] .DS_Store Added in .gitignore
```

## What Makes Commit Title, Perfect?

* Title case such as "This Sentence is Having Title Case"
* 50 characters or lesser
* Having a task ID prepended wrapped with a square bracket followed by a single space

# Description

Commit description is important part of commit history and helps a lot to reviewers of pull requests who are actually analysing your code against the task (probably) they assigned to you.

So for the sake of helping them to understand them (and as lesser questions) you should make it a little more subtle.

## Bad Examples

> "Too long & redundant."

```
[MGP-2] Scaffolded & Added Configuration Files

Added configuration files and scaffolded the project, the HOCON boilerplate is all removed from the configuration files. Then moved towards working on defining project architecture for rest of the code, folders and files - basically.
```

## Good examples

> "Perfect. Bullet-ed."

```
[MGP-2] Scaffolded & Added Configuration Files

* Configuration segregated
* Added basic project structure
* Added README.md for instructions to run
```

## What Makes Commit Description, Perfect?

* Bullet-ed
* Each line not ending with a dot
* Each line telling something that is not already mentioned in lines above
* First letter capital
