---
layout: post 
title:  "How do I configure proxy settings for LOCAL SYSTEM? - Server Fault" 
date:   2017-07-13T19:07:51.102Z 
categories: netsh winhttp proxy
link: https://serverfault.com/questions/34940/how-do-i-configure-proxy-settings-for-local-system 
tags:
  - links
ogtype: article 
---

## How do I configure proxy settings for LOCAL SYSTEM? - Server Fault
It is actually the value in Software\Microsoft\Windows\CurrentVersion\Internet Settings\Connections\DefaultConnectionSettings that is used.

Since that is not easily modified, you can modify the proxy settings for a user, export the registry key, modify the path in the exported file to HKEY_USERS\S-1-5-18 and reimport it.