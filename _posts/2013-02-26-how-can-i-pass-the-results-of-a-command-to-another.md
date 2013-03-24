---
layout: post-layout
title: How can I pass the results of a command to another?
tags:
- linux
---

The `xargs` program passes the outputs of one command as arguments to another
one.

The following is an example of processing the results of find using `xargs`:

    find . -name <pattern> -print0 | xargs -0 -I {} <command with {} as an argument>

`find -print0` and `xargs -0` make `find` and `xargs` handle files with unusual
characters in their names properly.

**References**

- http://linux.byexamples.com/archives/80/xargs-use-stardard-output-as-parameter-for-another-command
- http://www.cyberciti.biz/faq/linux-unix-bsd-xargs-construct-argument-lists-utility/
- http://www.gnu.org/software/findutils/manual/html_mono/find.html#Unusual-Characters-in-File-Names

