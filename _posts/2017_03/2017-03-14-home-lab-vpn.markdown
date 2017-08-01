---
layout: post 
title:  "Home Lab - VPN" 
date:   2017-03-14T21:59:35.620Z 
categories: homelab vpn vyos
link: https://www.darkoperator.com/blog/2017/2/5/home-lab-vpn 
tags:
  - links
ogtype: article 
---

> Home Lab - VPN

MARCH 09, 2017 BY CARLOS PEREZ
Since our lab is isolated from the home network behind the router we need a way to access the VM's inside from our research systems. To access the systems behind the router we can use a VPN. With VyOS we have 2 options:

L2TP/IPSec - Native support on Windows and OS X. Linux client support can be tricky.
OpenVPN - Requires third party client installed, works well on Windows, OS X and Linux.
Depending on your client machine the type of VPN solution will vary. In the case of Windows and OS X L2TP/IPSec works very well in my experience. When developing my tools on Linux, OpenVPN tends to be more stable. 

Configuring L2TP/IPSec VyOS

We start configuring L2TP/IPSec by first changing to configuration mode after logging in to the router and specifying the interface we will use for IPSec  connections. In addition to this I configured NAT Traversal, this step is not required it is only in the case one VM inside the network wants to VPN in to another environment.