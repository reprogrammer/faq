---
layout: post-layout
title: How can I include or exclude certain files from Git?
tags:
- git
---

Sometimes, you want to exclude all the (for instance) `.class` or `.jar` files
from git. In that case, you would create a `.gitignore` folder at the top of
your repository with contains like this:

    *.class
    *.jar

On the other hand, sometimes you also want to include certain `.class` or `.jar`
files in only several directories. In that case, you would create a `.gitignore`
in those particular directories like this:

    !*.class
    !*.jar

The key symbol here is the `!` symbol.

Git operates by reading the repository-level `.gitignore` but will override any
settings upon reading a directory-level `.gitignore`.

