---
layout: post-layout
title: How can I more easily view diffs from Git?
tags:
- git
---

Say that you want to see what has changed between two different commits. You can
do

    git diff sha1..sha2

The above command will give you all the differences between sha1 (exclusive) to sha2
(inclusive). However, textual diffs can be hard to understand sometimes, so how
would you specify a visual diff tool? The easiest way would be to specify the
name of the visual diff tool directly to git difftool i.e.

    git difftool -t path_to_tool sha1..sha2

If you find yourself using a particular visual diff tool pretty often, then you
should add it to your global git config file, shown with a hypothetical tool
called `awesometool`:

    git config --global diff.tool awesometool
    git config --global difftool.awesometool.cmd "path/to/awesometool \$LOCAL \$REMOTE"
    # The following gets rid of having to hit enter when you run git difftool
    git config --global difftool.prompt false

which will create the following entries in your global `.gitconfig`

    [diff]
      tool = awesometool
    [difftool "awesometool"]
      cmd = path/to/awesometool \"$LOCAL\" \"$REMOTE\"
    [difftool]
      prompt = false

Popular visual diff tools are
[vimdiff](http://vimdoc.sourceforge.net/htmldoc/diff.html),
[kdiff3](http://kdiff3.sourceforge.net/), [meld](http://meld.sourceforge.net/),
etc. You can specify several programs (not just a single one) that you use
frequently through the global git config.

    git difftool sha1..sha2

Once you add your visual diff tool to git configurations, you can simply invoke
`git difftool` as follows.

**References**  

- [http://stackoverflow.com/questions/255202](http://stackoverflow.com/questions/255202)

