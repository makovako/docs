---
title: 13 git tips
---

[00:00:40](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=40)

# 13 git and tricks

[00:01:19](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=79)

`git commit -am ""` - adds all files in current working directory

[00:01:37](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=97)

Git aliases:
`git config --global alias.ac "commit -am"`

[00:01:51](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=111)

`git commit --amend -m "new messgae" - update last commit message

[00:02:02](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=122)

`git commit --amend --no-edit` - add files to previous commit without changing message

[00:02:16](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=136)

`git push origin master --force` will overwrite remote repositoryoy with the local state, you might lose commits though

[00:02:31](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=151)

`git revert` - undo a commit with a new commit

[00:03:17](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=197)

hitting `.` on github repository opens up online vscode, if terminal needed, codespace can be used

[00:03:36](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=216)

`git stash` - remove changes and save them for later use

[00:03:50](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=230)

`git stash save name` - name your stash for reference

[00:03:56](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=236)

`git stash list`, `git stash apply index`

[00:04:24](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=264)

historicaly, master for main branch was used, to change it `git branch -M main`

[00:04:33](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=273)

`git log` - view history of commits

[00:04:43](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=283)

`git log --graph --oneline --decorate` - nicer log output

[00:05:15](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=315)

`git bisect` - find bad commit, mark start and end

[00:05:39](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=339)

Squashing commits - git rebase master -- interactive, opens editor

[00:05:50](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=350)

use squash before commits to squash them, or you can change commit messages as well

[00:06:10](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=370)

git commit --fixup or --squash when making commit

[00:06:16](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=376)

then use rebase with autsquash flag

[00:06:29](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=389)

git hooks - allows to run code before/after commit automatically

[00:07:13](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=433)

reset everything to be the same as on remote
`git fetch origin`
`git reset --hard origin/master`

[00:07:29](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=449)

`git clean -df` - clean random files and build artefacts

[00:07:40](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=460)

get rid off git - `rm -rf .git`

[00:07:49](https://www.youtube.com/watch?v=ecK3EnyGD8o&t=469)

`git checkout -` - go to previous branch

[source](https://www.youtube.com/watch?v=ecK3EnyGD8o)
