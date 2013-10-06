---
layout: post-layout
title: How can I push a local git branch and automatically track it?
tags:
- git
---

    git push -u origin <name_of_branch>

Git will by default push all branches that have the same name on the remote. To
limit this behavior to just the current branch, set this configuration option:

    git config --global push.default tracking

**References**  

- [http://mislav.uniqpath.com/2010/07/git-tips/](http://mislav.uniqpath.com/2010/07/git-tips/)

