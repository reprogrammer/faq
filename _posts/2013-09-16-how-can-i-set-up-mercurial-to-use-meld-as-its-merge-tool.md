---
layout: post-layout
title: How can I set up mercurial to use meld as its merge tool?
tags:
- mercurial
---
Add the following to `~/.hgrc`:

    [ui]
    merge = meld
     
    [merge-tools]
    meld.priority = 1
    meld.premerge = False
    meld.args = $local $other $base
     
    [merge-patterns]
    ** = meld

When meld opens the local (the working copy version), other (the remove version,
which is being merged into local), and base (common parent of local and other)
versions of the file, edit the middle pane (other), for this is the file in your
repository. The other two are kept in `/tmp`.

**References**  

- [http://stackoverflow.com/q/10115412/130224](http://stackoverflow.com/q/10115412/130224)

