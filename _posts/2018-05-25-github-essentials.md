---
layout: post
tags: github
date: 2018-05-25 
thumbnail: https://tech.bodyfitstation.com/wp-content/uploads/2016/11/github-logo.png
title: GitHub Essentials Kitty
published: true
---

Testing a Pull Request
----------------------

This can be very helpful when you want to find bugs and test out new features before they get merged into the main project.

How to checkout a pull request on your own computer?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
```
git fetch upstream pull/<id>/head:<branch>
git checkout <branch>
```

* where `id` is the PR number,
* ...and `branch` refers to the author's branch

Git aliases to help you get a Pull Request
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Aliases are shortcuts that you can define in git bash (or linux/mac) that 
reduces typing and minimizes errors. 

*Grabbing a PR and switching to that branch*
```bash
git config --global --add alias.pr '!f() { git fetch -fu ${2:-upstream} refs/pull/$1/head:pr/$1 && git checkout pr/$1; }; f'
```

*Deleting the branch*
```bash
git config --global --add alias.pr-clean '!git checkout master ; git for-each-ref refs/heads/pr/* --format="%(refname)" | 
while read ref ; do branch=${ref#refs/heads/} ; git branch -D $branch ; done'
```

*Usage*

To pull a pull request: `git pr <id>` (example: `git pr 123`)

To delete all the pull requests created with git pr alias: `git pr-clean`

References
~~~~~~~~~~
* https://github.com/TeamPorcupine/ProjectPorcupine/wiki/How-to-Test-a-Pull-Request[ProjectPorcupine Wiki] 
