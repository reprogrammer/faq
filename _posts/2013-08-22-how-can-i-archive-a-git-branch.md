---
layout: post-layout
title: How can I archive a Git branch?
tags:
- git
---

Instead of just deleting a branch, it might be a good idea to keep a tag to the
old branch.

    # Get remote branches verbosely (with SHA and some description)
    git branch -a -v
    # Pick the old branch that you want to archive and note its SHA
    git tag archive/<old-branch-name> <old-branch-SHA>
    # Delete the local branch
    git branch -d <old-branch-name>
    # Push the tag to remote repository
    git push --tags
    # Delete the remote branch
    git push origin :<old-branch-name>
    # (Optional for other people monitoring the remote repository)
    # This removes outdated branches from their local repository
    git remote prune origin

**References**

- [http://stackoverflow.com/questions/1307114](http://stackoverflow.com/questions/1307114)

