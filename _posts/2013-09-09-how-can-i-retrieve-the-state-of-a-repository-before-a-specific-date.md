---
layout: post-layout
title: How can I retrieve the state of a repository before a specific date?
tags:
- git
---

    git checkout `git rev-list -n 1 --before="2009-07-27 13:37" master`

**References**  

- [http://stackoverflow.com/a/6990682](http://stackoverflow.com/a/6990682) 

