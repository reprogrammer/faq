---
layout: post-layout
title: How can I create shorthands for Git commands?
tags:
- git
---

Set up aliases in your global `~/.gitconfig`. Here's a set of useful examples
that you can add to your `~/.gitconfig` file:

    [alias]
      st = status
      ci = commit
      br = branch
      co = checkout
      df = diff
      lg = log -p

Now, you can use `git st` instead of `git status`.

**References**  

- [http://www.gitready.com/intermediate/2009/02/06/helpful-command-aliases.html](http://www.gitready.com/intermediate/2009/02/06/helpful-command-aliases.html)

