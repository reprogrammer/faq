---
layout: post-layout
title: How can I debug a test run by Maven in IntelliJ IDEA?
tags:
- intellij
---

Open the Maven Projects view, and then open the Lifecycle tree item. Next,
right-click on the test goal to creat a configuration. Add the command-line
option `-DforkMode=never` to the configuration. Finally, run the configuration
in debug mode.

**References**  

- [http://stackoverflow.com/q/3784781](http://stackoverflow.com/q/3784781)

