---
layout: post 
published: true 
title: "Citrix NetScaler Gateway - Installation, configuration and integration with XenApp/XenDesktop - Citrix - InformatiWeb Pro" 
date: 2016-08-29T03:57:12.113Z
categories: citrix netscaler networking
link: http://us.informatiweb-pro.net/virtualization/1-citrix/18--citrix-netscaler-gateway-installation-configuration-and-integration-with-xenapp-xendesktop.html 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## Citrix NetScaler Gateway - Installation, configuration and integration with XenApp/XenDesktop - Citrix - InformatiWeb Pro

 NetScaler Gateway is a gateway created by Citrix that allows you to use the load balancing system and provides a secure remote access to applications and desktops published through XenApp, XenDesktop and XenMobile.

In this tutorial, we will install NetScaler Gateway on our XenServer server to provide a secure remote access to our applications published with XenApp.
Nevertheless, the procedure is the same for desktops published with XenDesktop.

Configuration used :

Server 1 / IP : 10.0.0.101 / A server under Win. Server 2012 with an Active Directory (and a root certification authority created to avoid paying SSL certificate)
Server 2 / IP : 10.0.0.102 / A server under Win. Server 2012 where XenApp 7.6 is installed. (This server is linked to the Active Directory)
Server 3 / IP : 10.0.0.103 / A server under Win. Server 2012 where the Virtual Delivery Agent is installed and applications that we have already published in XenApp.
Server 4 / IP : 10.0.0.105 / The virtualization server XenServer 6.2.
Server 5 / NetScaler Gateway with 3 IP addresses (NSIP, SNIP and VIP) as explained in the tutorial and in the diagram below.
1 computer under Windows or with another operating system to test the remote access to applications and desktops available through XenApp. (The computer must be on the outside of your local network or on Internet *)
* To simulate an external access, you need a PC that is outside of the local network where are your servers under Windows Server.
For this, you have 2 options :

