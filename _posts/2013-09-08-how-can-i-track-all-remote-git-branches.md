---
layout: post-layout
title: How can I track all remote Git branches?
tags:
- git
---

First, get a list of all remote branches:

    git branch -r

Then, check out each of remote branch:

    git checkout -t origin/branch1

**References**  

- [http://stackoverflow.com/questions/67699/how-do-i-clone-all-remote-branches-with-git](http://stackoverflow.com/questions/67699/how-do-i-clone-all-remote-branches-with-git)

