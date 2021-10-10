---
title: "Git for professionals"
---

[00:01:33](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=93)

# The perfect commit

[00:01:40](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=100)

1. add the right changes
2. compose a good commit message

[00:01:58](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=118)

create commits that makes sense, that contains only single topic

[00:02:37](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=157)

more changes = harder to understand the commit

[00:03:56](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=236)

`git diff filename` - list changes only in single file

[00:04:24](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=264)

`git add -p` - add only part of a file to staging area = patch level

again, filename can be specified to make it easier and don't go through big files which we don't want to commit at all

[00:06:05](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=365)

Perfect commit message

- subject - summary of what happened
- body - more detailed explanation
  - what is now different than before
  - what's the reason for the change
  - anything to watch out for

[00:06:24](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=384)

if it's difficult to write commit summary, it might mean the commit is big and can be separated

[00:08:12](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=492)

# Branching strategies

[00:09:09](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=549)

Various possibilities for branching strategies, needs to be discussed in a team and written convention should be created.

[00:09:42](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=582)

Integrating changes and structuring releases (two extremes mentioned)

- mainline development
- state, release and feature branches

[00:10:07](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=607)

## Mainline development

- always be integrating
- one main branch, integrate often
- few branches for development, small commits, high quality testing and QA standards

[00:11:03](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=663)

## State, Release, Feature Branches

- multiple branches
- different types of branches with their specific meaning

[00:11:21](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=681)

Many types of branches here:

- features and experiments
- main or release branch
- development branches
- different stages of workflow: development, release, production branches

[00:11:53](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=713)

### Long-running and short-lived branches

[00:12:30](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=750)

Long-running branches

- they exist through the whole lifecycle of a project
- main/master

[00:12:54](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=774)

Integration branches:

- states of the project release or deployment
- develop or staging

[00:13:22](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=802)

Usually no direct commits are allowed to the long-running branches. Only through merge or rebase.

[00:14:01](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=841)

Also better monitoring of what is going to be released.

[00:14:15](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=855)

Short-lived branches

- created for certain purpose, deleted afterward
- new features, bug fixes, refactoring, experiments

[00:14:49](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=889)

Base the short branch on the long branch, create changes, merge or rebase them back into long branch and delete the short one.

[00:15:10](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=910)

## Examples of branching strategies

- GitHub Flow
- GitFlow

[00:15:24](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=924)

### GithubFlow

- one long running branch, everything else in short lived branches

[00:15:46](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=946)

### GitFlow

- more structure
- main branch represents production state
- develop branch holds delevelopment, any feature branch stats and ends here
- main and develop are long-lived branches
- also any release branch for QA starts here
- when everything works, release branch is merged to production for release, creates tags and closes release branches

[00:17:15](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=1035)

Branching workflow depends on team, can take inspirations from gitflow and github flow.

[00:17:20](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=1040)

# Pull requests

[00:17:31](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=1051)

- provided on git hosting platforms

[00:17:53](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=1073)

- communicate code and review it

[00:18:17](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=1097)

- someone else can look at your code before it gets merged

[00:18:45](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=1125)

- also only way to contribute to other repositories where you don't have write access

[00:19:13](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=1153)

- fork - personal copy of git repository

[00:21:26](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=1286)

- pull requests are based on branches, not individual commits

[00:22:04](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=1324)

- `git branch test`, `git checkout test`, `git checkout -b test`

[00:23:41](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=1421)

- fork, clone yours, create branch, commit, push, create pull request

[00:24:08](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=1448)

# Merge conflicts

[00:24:25](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=1465)

- when they happen
- what they are
- how to solve them

[00:24:49](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=1489)

They can happen:

- when integrating changes
- when merging or rebasing
- when pulling, cherry-picking or applying stash

[00:25:29](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=1529)

most of the time integrating changes works fine, only when contradictory changes are made, git can't decide which one is the right one

[00:26:42](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=1602)

When conflict occurs:

- git tells immediately, that you have unmerged paths

[00:27:59](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=1679)

Undoing conflict:

- `git merge --abort`, `git rebase --abort`

[00:29:33](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=1773)

How the config looks like

- it has lines marked with what comes from where, with symbols like `<<<<`, `=====`, `>>>>`

[00:30:31](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=1831)

conflict can occure, e.g.

- line was deleted in one branch and changed in another one

[00:30:49](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=1849)

solving the conflict = clean up this lines

[00:33:08](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=1988)

After cleanup, the changes needs to be commited

[00:33:25](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=2005)

file.orig - safety copy of a file between the conflict and cleanup commit

[00:33:51](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=2031)

# Merge vs Rebase

[00:34:06](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=2046)

- getting new code back into existing branch

[00:34:17](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=2057)

## Merge

[00:34:32](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=2072)

Merges looks for 2 commits:

- common ancestor commit
- last commit on one branch
- last commit on the second branch

[00:35:24](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=2124)

Fast-forward merge, when commits in feature branch can be added to main branch just by adding them, because there are ano new commits in the main branch

[00:35:45](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=2145)

When there are new changes in main branch, new commit needs to be created, called merge commit, which contains the differences between branches

[00:36:12](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=2172)

Merge commit is created automatically by git, and it's purpose is to connect two branches, also the commit message doesn't explain content of a commit

[00:37:03](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=2223)

## Rebase

- sometimes we want clean history, only want to see what happened, what;s in the commits, without any merge commits
- rebase is not better/worse then marge, ti's different

[00:37:30](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=2250)

- `git rebase feature-branch` - which branch we want to integrate (same for merge)

[00:37:39](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=2259)

1. git removes commits on main branch into parking area, which are after the common ancestor commit

[00:37:56](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=2276)

2. git applies new commits from feature branch

[00:38:15](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=2295)

3. parked commits are integrated, rebased

[00:38:27](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=2307)

looks like development happened in straight line, we preserve the original commit structure

[00:38:34](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=2314)

rebase rewrites commit history

[00:38:52](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=2332)

original commits are new commits, because they will have a new parent after the rebase, originally it was the common ancestor, after rebase it will be last commit in the feature branch

[00:39:30](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=2370)

don't rewrite history, that has already been pushed, it might make trouble for others

[00:39:36](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=2376)

somebody might have been branched off the commit, you have changed/rebased

[00:39:44](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=2384)

Do not rewrite commits, that has been already pushed into remtoe repository

[00:40:04](https://www.youtube.com/watch?v=Uszj_k0DGsg&t=2404)

Use rebase for cleaning you local commit history, before merging it into a shared team branch

[source](https://www.youtube.com/watch?v=Uszj_k0DGsg)
