---
layout: post-layout
title: How can I delete all Git branches that have been merged?
tags:
- git
---

    git branch -r --merged | \ 
    grep origin | \
    grep -v '>' | \
    grep -v master | \
    xargs -L1 | \
    awk '{split($0,a,"/"); print a[2]}' | \
    xargs git push origin --delete

**References**  

- [https://gist.github.com/942899](https://gist.github.com/942899)

