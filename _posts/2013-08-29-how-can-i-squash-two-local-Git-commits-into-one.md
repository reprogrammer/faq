---
layout: post-layout
title: How can I squash two local Git commits into one?
tags:
- git
---

Use the following commit to start `rebase` in the interactive mode. You should
use a `<SHA>` that is a ascendant of the commits you want to manipulate.

    git rebase -i <SHA>

The interactive `rebase` lets you perform a command on each commit that it
lists.  If you want to squash `commit 2` into `commit 1`, you should make sure
that the `rebase` editor shows you only the two commits, then you have to use
the pick command on `commit 1` and the `squash` command on the line of `commit
2`.

If for any reason, you have to quit the rebase, close the editor and execute the
following command.

    git rebase --abort

