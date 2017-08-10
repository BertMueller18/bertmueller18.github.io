---
layout: post 
published: true 
title: "IPv6 – Disabling isatap Teredo and 6to4 in Windows 7 | The Internet made me do it!" 
date: 2016-07-05T09:28:04.193Z
categories: ipv6 teredo windows
link: http://www.dickson.me.uk/2012/03/20/ipv6-disabling-isatap-and-6to4-in-windows-7/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## IPv6 – Disabling isatap Teredo and 6to4 in Windows 7
Posted on March 20, 2012
To disable isatap teredo and 6to4 on a Windows 7 workstation, type the following at the prompt. You do of course need Administrative access on the workstation to do this.

If like myself your running dual stack IPv6 via your router or gateway, then there is really no need to have them running.


```shell
netsh int ipv6 isatap set state disabled
netsh int ipv6 6to4 set state disabled
netsh interface teredo set state disable
```

Thanks for the input guys, I’ve changed the following to set it back to default.

To re-enable isatap teredo nd 6to4, just replace the disabled with type=default.

R