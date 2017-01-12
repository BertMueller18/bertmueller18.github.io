---
layout: post
published: true
title: "Activating a Windows 2012 R2 Server offline | Johnny BizTalk"
date: 2016-11-10T20:46:48.945Z
categories: activedirectory kms security 
categories: server2012 kms
link: https://blogs.msdn.microsoft.com/joscot/2014/10/15/activating-a-windows-2012-r2-server-offline/
tags:
  - links
ogtype: article
bodyclass: post
---

> Activating a Windows 2012 R2 Server offline

If you’re trying to activate a server which has no internet connectivity or access to a KMS server, your options for activating Windows are narrowed to calling the automated phone service.  In previous versions of Windows, it would prompt you to enter a product key, then ask if you would like to activate over the internet.  If you declined, you’d be given the phone option.

In Windows Server 2012 R2 the behavior is different, in that when you activate the product key, you are simply told that it is an invalid key.  In truth, the server is trying to validate the key over the internet, which of course doesn’t work if your server doesn’t have a path out.

The key (ahem) is a couple of command lines:

slmgr -ipk XXXXX-XXXXX-XXXXX-XXXXX-XXXXX (where “X” is your product key)

slui 4

This will bring up the UI, similar to previous Windows versions, that will walk you through phone activation.
