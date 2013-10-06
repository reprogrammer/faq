---
layout: post-layout
title: How can I find the common ancestor of two Git branches?
tags:
- git
---

There isn't a command to find the common ancestor per-se, but there is a
plumbing command, `git-merge-base` in Git for finding the best ancestor for use
in a three-way merge. Given a series of branches, `git-merge-base` attempts to
find the best ancestor to merge. When you provide it with two branches as
arguments, `git-merge-base` will naturally locate their common ancestor, if one
exists. This can be useful sometimes when you are trying to trace the common
ancestor between branches.

    git-merge-base branchA branchB

