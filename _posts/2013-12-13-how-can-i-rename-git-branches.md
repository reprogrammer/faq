---
layout: post-layout
title: How can I rename Git branches?
tags:
- git
---

The following command renames a local branch from `b1` to `b2`.

    git branch -m b1 b2 

The following command removes the remote branch `b1`.

    git push origin --delete :b1

Before running the above command, make sure that `b1` is not the default branch
of your repository; otherwise, git will give you an error like the following.

    remote: error: refusing to delete the current branch: refs/heads/b1
    To https://github.com/user/repo.git
     ! [remote rejected] b1 (deletion of the current branch prohibited)
    error: failed to push some refs to 'https://github.com/user/repo.git'

The following command gives `b2` the new remote.

    git push -u origin b2

**References**  

- [http://stackoverflow.com/a/7084316](http://stackoverflow.com/a/7084316)
- [http://sebgoo.blogspot.com/2012/04/git-rename-branch-local-and-remote.html](http://sebgoo.blogspot.com/2012/04/git-rename-branch-local-and-remote.html)
- [http://stackoverflow.com/a/2003515](http://stackoverflow.com/a/2003515)

