---
title: How to change the keyboard layout in Busybox.
date: 2018-02-14 14:22:00 -02:00
layout: post
---

Create and change to a own .kmap

Mybe you asked your self this question too. I my self took a while till i found out that i can create a own .kmap file within Busybox.

The only thing it needs, is a terminal with a working keyboard layout, witch you like to crete.

In the terminal you type :


```
sudo busybox dumpkmap > yourkeymapfile.kmap 

```
whenever you like it you can load it with:

```
busybox loadkmap < yourkeymapfile.kmap

```



