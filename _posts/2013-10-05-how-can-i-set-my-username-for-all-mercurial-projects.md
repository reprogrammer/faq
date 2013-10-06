---
layout: post-layout
title: How can I set my username for all Mercurial projects?
tags:
- mercurial
---
Add the following piece of code to your `.hgrc` file.

    [ui]
    username = FirstName LastName <username@domain.com>

