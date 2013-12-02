---
layout: post-layout
title: How can I install Ubuntu repository public keys?
tags:
- linux
---

If you get an error like the following from `apt`:

>W: GPG error: http://ppa.launchpad.net lucid Release: The following signatures
>couldn't be verified because the public key is not available: NO_PUBKEY
>A6DCF7707EBC211F

Take the last 8 characters of the string in the error message and use it in the
following two commands:

    gpg --keyserver keyserver --recv 7EBC211F

The *keyserver* in the above commands may be a server like
`keyserver.ubuntu.com` or `pgp.mit.edu`.

The above command will generate an output similar to the following:

>gpg: requesting key 7EBC211F from hkp server keyserver.ubuntu.com
>gpg: key 7EBC211F: public key "Launchpad PPA for Ubuntu Mozilla Security Team" imported
>gpg: no ultimately trusted keys found
>gpg: Total number processed: 1
>gpg:               imported: 1  (RSA: 1)

Next, run the following command:

    gpg --export --armor 7EBC211F | sudo apt-key add -

The above command should generate the following output:

>OK

Note the post at [http://askubuntu.com/a/127187](http://askubuntu.com/a/127187)
suggest that the above two steps can be performed in a single steps. I need to
try out this command.

    sudo apt-key adv --keyserver keyserver --recv-keys 7EBC211F

**References**

- [http://www.univet.hu/users/jkis/Education/Linux/Linux_repositories.txt](http://www.univet.hu/users/jkis/Education/Linux/Linux_repositories.txt)

