---
layout: post-layout
title: How can I resolve Git merge conflicts visually?
tags:
- git
---

You can use a visual merge tool like
[diffmerge](http://www.sourcegear.com/diffmerge/). You would use the same
command to git visual diff except that you use `git mergetool` instead of `git
difftool`.

    git config --global merge.tool awesometool
    git config --global mergetool.awesometool.cmd "path/to/awesometool --merge --result=\"$MERGED\" \"$LOCAL\" \"$BASE\" \"$REMOTE\""
    git config --global mergetool.awesometool.trustExitCode true

**References**  

- [http://stackoverflow.com/questions/585844](http://stackoverflow.com/questions/585844)

