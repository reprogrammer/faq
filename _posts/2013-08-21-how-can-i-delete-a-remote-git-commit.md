---
layout: post-layout
title: How can I delete a remote git commit?
tags:
- git
---

If you push a commit to the remote repository. You can remove it from the remote
repository using the following command.

    git push -f origin HEAD^:master

I've tried this command on github and made sure that it works. As a result of
this command, your commit on the remote repository doesn't get actually deleted.
Rather, it becomes dangling. And, it seems that [Github garbage collects
dangling commits every so often](http://stackoverflow.com/questions/4367977).

**References**

- [http://stackoverflow.com/questions/448919](http://stackoverflow.com/questions/448919)

