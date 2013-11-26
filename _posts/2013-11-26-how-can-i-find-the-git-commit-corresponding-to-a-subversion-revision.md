---
layout: post-layout
title: How can I find the Git commit corresponding to a Subversion revision?
tags:
- git
- subversion
---

Let *S* be the URL of a Subversion repository that has been migrated to a Git
repository at URL *G* using
[git-svn](https://www.kernel.org/pub/software/scm/git/docs/git-svn.html). Given
the revision number *R* of a revision of *S*, the problem is to find a commit
*C* in *G* that corresponds to *R*.

For example, let *S* = http://svn.apache.org/repos/asf/1309183/tomcat/trunk/,
*G* = https://github.com/apache/tomcat.git, and *R* = 1309183.

The first step is find the largest revision number *R2* such that *R2* <= *R*
and *S* is affected by *R2*. The following command will return *R2*.

    svn list --verbose S@R | grep "\./" | awk '{split($0,a," "); print a[1]}'

In this case, the above command would look as follows.

    svn list --verbose http://svn.apache.org/repos/asf/tomcat/trunk/@1309183 | grep "\./" | awk '{split($0,a," "); print a[1]}'

Next, use a command of the form below to find *C*.

    git log | grep "@R2" -C 10

In this case, the above command should be instantiated as follows.

    git log | grep "@1307597" -C 10

**References**  

- [http://stackoverflow.com/a/1633683](http://stackoverflow.com/a/1633683)

