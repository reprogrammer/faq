---
layout: post-layout
title: How can I browse the history of a Mercurial repository graphically?
tags:
- mercurial
---
Enable the `hgk` extension by adding the following to your `.hgrc` file.

    [extensions]
    hgk =

Then, invoke the following command inside the directory of your mercurial
repository:

    hg view

**References**  

- [http://mercurial.selenic.com/wiki/HgkExtension](http://mercurial.selenic.com/wiki/HgkExtension)

