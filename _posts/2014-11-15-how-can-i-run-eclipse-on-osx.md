---
layout: post-layout
title: How can I run Eclipse on OS X?
tags:
- osx
- eclipse
---

- Run `/usr/libexec/java_home -V` to find the location of an installed JDK.
- To launch Eclipse from Finder, follow the instructions at
  [http://stackoverflow.com/a/25486012/130224](http://stackoverflow.com/a/25486012/130224)
to set the `-vm` flag of `Eclipse.app/Contents/Info.plist`.
- To run Eclipse from the command line, run
  `Eclipse.app/Contents/MacOS/eclipse`.

**References**  

- [http://stackoverflow.com/a/25486012/130224](http://stackoverflow.com/a/25486012/130224)

