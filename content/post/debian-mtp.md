+++
categories = ["Linux"]
date = "2017-06-13T05:13:08+03:00"
tags = ["linux", "debian", "android", "mtp"]
title = "Connecting MTP device on Debian 8"
+++

Finally I succeeded with connecting my Android device via MTP protocol.

Command line solution was quite easy. But it took some time for me to try few possible solutions.

Full instructions can be found on [Debian wiki](https://wiki.debian.org/mtp#Commandline). But I'll make some notes for myself here.

Setup `jmtpfs`

```
# aptitude install jmtpfs
```

Create mount folder and setup rights

```
# mkdir /media/Phone
$ sudo chown $USER:$USER /media/Phone
```

Plug-in device and mount it

```
$ jmtpfs /media/Phone
```

Unmount with

```
$ fusermount -u /media/Phone
```

<!--more-->

P.S. I want my "USB storage device" mode back. :(