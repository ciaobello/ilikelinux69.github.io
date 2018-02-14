---
title: How to change the keyboard layout in Busybox.
date: 2018-02-14 14:22:00 -02:00
layout: post
---

Create and change to a own .kmap with Busybox.

Mybe you asked yourself this question too. I myself took a while till i found out that i can create a own .kmap file within Busybox.

The only thing it needs, is a terminal with a working keyboard layout, witch you like to create.

In the terminal you type :


``` busybox dumpkmap > yourkeymapfile.kmap ```


whenever you like it you can load it with:

``` busybox loadkmap < yourkeymapfile.kmap ```




