---
layout: post-layout
title: How can I apply a commit from one Git branch to another?
tags:
- git
---

Let `s` be the SHA of the commit you'd like to apply to branch `b`. Execute the
following commands to add commit `s` to branch `b`.

    git checkout b
    git cherry-pick s

