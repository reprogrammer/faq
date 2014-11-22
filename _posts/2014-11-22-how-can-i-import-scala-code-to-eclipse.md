---
layout: post-layout
title: How can I import Scala code to Eclipse?
tags:
- eclipse
- scala
---

Add sbteclipse to your plugin definition file. For sbt version 0.13 and up, add
the following to `~/.sbt/0.13/plugins/plugins.sbt`.

    addSbtPlugin("com.typesafe.sbteclipse" % "sbteclipse-plugin" % "2.5.0")

**References**  

- [https://github.com/typesafehub/sbteclipse](https://github.com/typesafehub/sbteclipse)

