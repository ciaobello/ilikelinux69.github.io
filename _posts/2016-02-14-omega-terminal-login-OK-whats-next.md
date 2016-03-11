---
layout: post
title:  "Omega-Terminal-Login OK, whats next?"
date:   14-02-2016 19:17:00 -0200
categories: jekyll update
---
~~~
     BusyBox v1.23.2 (2016-01-28 00:00:02 UTC) built-in shell (ash)
     ONION OMEGA
     W H A T  W I L L  Y O U  I N V E N T ?

     -----------------------------------------------------
     Ω-ware: 0.0.6 b275
     -----------------------------------------------------
     root@Omega-24CF:~#
~~~
If you are not used to work with the terminal, you might be happy to get some additional information what you can do within this "**Black-Box**".

To get more info about what commands you can use just type:

     busybox --help

and you will get a overview of what busy-box is and all commands available over it.

     busybox --list

if you prefer a list of all this commands.

If you need more explanation about a certain command just use:

     busybox ifconfig --help

(ifconfig is the equivalent of **ipconfig** in Windows)


Several times I also read people asking which openWRT is running.

The release/version files can be made visible with:

      cat /etc/*_release

or

      cat /etc/*_version


Further information about the base of Omega OS you find by openWRT
https://wiki.openwrt.org/doc/howto/user.beginner.cli


