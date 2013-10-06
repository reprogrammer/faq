---
layout: post-layout
title: How can I restore a particular version of a file from a Git repository?
tags:
- git
---

The following command will replace the current version with the older version.
If you just want to see the older version of the file, use `git show`.

    git checkout SHA1 path/to/file

**References**  

- [http://www.kernel.org/pub/software/scm/git/docs/user-manual.html#checkout-of-path](http://www.kernel.org/pub/software/scm/git/docs/user-manual.html#checkout-of-path)

