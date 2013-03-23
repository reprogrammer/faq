---
layout: post-layout
title: How can I install ant without GCJ?
tags:
- linux
---

```
sudo apt-get install --no-install-recommends ant
```

When trying to use ant to build the X10 compiler, ant complained about a missing
JAR. It looked like the `build.xml` file used `javah` targets. So, I installed
ant-optional using the following command.

```
sudo apt-get install --no-install-recommends ant-optional
```
