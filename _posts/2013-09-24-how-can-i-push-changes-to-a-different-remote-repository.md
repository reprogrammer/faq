---
layout: post-layout
title: How can I push changes to a different remote repository?
tags:
- mercurial
---
First, add the path to the remote repository to `.hg/hgrc`.

    [paths]
    remote-name = http://path/to/remote-name

Then, push the changes in your local repository to the remote repository:

    hg push remote-name

If your changes belong to new branches, use the following command:

    hg push --new-branch remote-name

**References**

- [http://stackoverflow.com/a/3979215/130224](http://stackoverflow.com/a/3979215/130224)
- [http://stackoverflow.com/a/4959205/130224](http://stackoverflow.com/a/4959205/130224)

