---
layout: post-layout
title: How can I import a Bitbucket repository to GitHub?
tags:
- mercurial
- git
---

Run the following commands to install git remote hg.

    wget https://raw.github.com/felipec/git/fc/master/git-remote-hg.py -O ~/apps/git-remote-hg
    chmod +x ~/apps/git-remote-hg
    export PATH=$PATH:~/apps

Clone the mercurial repository as a bare git repository.

    git clone --bare "hg::https://code.google.com/p/jsr308-langtools/" bare-jsr308-langtools

Create an empty GitHub repository

    git push --mirror https://github.com/reprogrammer/jsr308-langtools.git

Mirror the bare git repository on github.

    cd bare-jsr308-langtools
    git push --mirror https://github.com/reprogrammer/jsr308-langtools.git

**References**  

- [https://github.com/felipec/git/wiki/git-remote-hg](https://github.com/felipec/git/wiki/git-remote-hg)
- [https://help.github.com/articles/importing-an-external-git-repository](https://help.github.com/articles/importing-an-external-git-repository)

