---
layout: post-layout
title: How can I merge Git branches?
tags:
- git
---

    git merge <branch_1> <branch_2>

The order which you specify the branch has some consequence on how it is done
internally. Graphically it will try to merge `<branch_1>` first and then
`<branch_2>` even if `<branch_2>` is earlier time-wise. So, if you want to have
a nice ordering, try to specify the earlier branch as an earlier argument.

