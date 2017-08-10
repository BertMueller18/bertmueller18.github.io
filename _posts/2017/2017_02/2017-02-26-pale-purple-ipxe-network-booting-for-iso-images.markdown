---
layout: post 
title:  "Pale Purple - iPXE Network booting for ISO images" 
date:   2017-02-26T08:10:31.222Z 
categories: ipxe
link: https://www.palepurple.co.uk/ipxe-network-booting-iso-images 
tags:
  - links
ogtype: article 
---

> iPXE Network booting for ISO images
 April 11, 2014,  palepurple, linux, systems administration, ,  0

Historically we had a ‘normal’ pxe boot server in the office (DHCP server points to a TFTP server and specified a pxelinux file to load) from which we could choose to install various distributions.

The only problem with this is that it was initially limited to the a specific release/version of Debian/Ubuntu (as we’d just copy the bundled install/netboot stuff locally).