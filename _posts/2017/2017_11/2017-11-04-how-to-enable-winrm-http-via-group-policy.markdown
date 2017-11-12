---
layout: post 
title:  "How to enable WinRM (HTTP) via Group Policy" 
date:   2017-11-04T19:18:58.573Z 
categories: powershell gpo activedirectory winrm
link: http://www.vkernel.ro/blog/how-to-enable-winrm-http-via-group-policy 
tags:
  - links
ogtype: article 
---

> How to enable WinRM (HTTP) via Group Policy
Windows Remote Management or WinRM for short, exist in the Windows world for a long time and until now you probably never had anything to do with it. WinRM is a Microsoft implementation of WS-Management Protocol, that allows hardware and operating systems, from different vendors, to interoperate. If enabled, you can run scripts, install roles and features on servers and clients or run the Remote Shell command line tool, and all this remotely. Practically you can do everything on a remote station the same way you are doing it locally. It is enabled by default on Windows server 2012/R2 but disabled on all client platforms and servers prior to server 2012. If for some reason you are still running Windows XP or server 2003, which are End of Life (EOL) now, you will need to install the Windows Management Framework Core package for this to work, since WinRM is not part of these operating systems. The service can be configured in two ways: secured (HTTPS) or un-secured (HTTP) and in this article I will treat the last one since it doesn’t require a complex infrastructure and configuration.
