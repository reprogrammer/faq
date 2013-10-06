---
layout: post-layout
title: How can I destroy my last Git commit and its changes?
tags:
- git
---

    git reset --hard ORIG_HEAD

Basically, `ORIG_HEAD` is short for the commit before your last commit. It's
automatically set by pull and merge (but not necessarily other git commands).
It's also equivalent to `HEAD@{1}` meaning the previous commit from head.

**References**  

- [http://stackoverflow.com/questions/964876](http://stackoverflow.com/questions/964876)

