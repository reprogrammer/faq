---
layout: post-layout
title: How can I pull changes to submodules?
tags:
- git
---

You have to go to the submodule and switch to a specific branch to be able to
pull changes.

    cd subproject-path
    git checkout branch-name
    git pull

**References**  

- [http://chrisjean.com/2009/04/20/git-submodules-adding-using-removing-and-updating/](http://chrisjean.com/2009/04/20/git-submodules-adding-using-removing-and-updating/)

