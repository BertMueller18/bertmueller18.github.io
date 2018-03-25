---
layout: post 
title:  "Remote Server Management for Large Enterprises - IronBrick" 
date:   2018-03-25T15:17:51.621Z 
categories: powershell automation activedirectory vmware
link: http://www.ironbrick.com/remote-server-management-for-large-enterprises/ 
tags:
  - links
ogtype: article 
---

> Remote Server Management for Large Enterprises
Part Three
By Dheeraj Advani
Automation Engineer, IronBrick

In the first two installments, the series covered how to set up a server for remote configuration and some examples of how to use WINRM to perform management activities. But what about standing up new servers? The issue is that when a virtual machine is first created, it won’t be accessible through WINRM. Fortunately, we can solve this problem by leveraging PowerShell and VMware’s “VMware Tools.”

VMware Tools are widely used in the industry for the management and tracking of VMs throughout the enterprise. However, there is huge untapped potential to perform management functions by leveraging the tools’ ability to execute commands on the guest OS of virtual machines. Paired with the right code snippets, they can become exceptionally useful.

