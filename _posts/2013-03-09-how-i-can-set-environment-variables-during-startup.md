---
layout: post-layout
title: How can I set environment variables during startup?
tags:
- linux
---

If you want to make an environment variable visible system-wide, you should set
it in `/etc/environment`. To set environment variables per user, you have to
modify `~/.pam_environment`.

The following is a sample `~/.pam_environment` file contents.

    JAVA_HOME  OVERRIDE=/path/to/java/home
    PATH       OVERRIDE=${PATH}:${JAVA_HOME}/bin

I've always had problems with `~/.pam_environment` for it duplicates my entries
in `PATH`. So, I use the system-wide configuration file, i.e.,
`/etc/environment`.

**References**

- [https://help.ubuntu.com/community/EnvironmentVariables](https://help.ubuntu.com/community/EnvironmentVariables)
- `man pam_env`
- `/etc/security/pam_env.conf`

