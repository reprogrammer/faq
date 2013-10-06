---
layout: post-layout
title: How can I remove a submodule from a Git repository?
tags:
- git
---

1. Delete the relevant section from the `.gitmodules` file.
1. Delete the relevant section from `.git/config`.
1. Run `git rm --cached subproject-path` (no trailing slash).
1. Commit and delete the now untracked submodule files.

**References** 

- [http://stackoverflow.com/a/1260982](http://stackoverflow.com/a/1260982)

