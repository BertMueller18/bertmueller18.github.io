---
layout: post 
title:  "[SOLVED] How to make UEFI bootable USB or DVD to install Server 2012 R2 - Spiceworks" 
date:   2017-04-27T06:42:21.213Z 
categories: deployment usb windows
link: https://community.spiceworks.com/topic/762943-how-to-make-uefi-bootable-usb-or-dvd-to-install-server-2012-r2 
tags:
  - links
ogtype: article 
---

I believe to make a usb bootable for UEFI it has to be FAT32

So you could open CMD and run this:

diskpart

list disk

select disk # (# is the value that represents your USB)

clean

create partition primary

select partition 1

format fs=fat32 quick

active

exit

Hopefully this is what you were looking for. 