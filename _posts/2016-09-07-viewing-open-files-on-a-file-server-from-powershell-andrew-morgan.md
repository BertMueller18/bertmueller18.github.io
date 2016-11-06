---
layout: post 
published: true 
title: "Viewing open files on a file server from powershell. | Andrew Morgan" 
date: 2016-09-07T11:27:57.120Z 
link: http://andrewmorgan.ie/2012/12/viewing-open-files-on-a-file-server-from-powershell/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Viewing open files on a file server from powershell.
2 Comments
So this is a situation you should all be aware of in an SBC / VDI environment, despite all warnings, you’ve redirected folders to your network drive and your file servers are screaming in agony?

Having been in this situation recently, I needed to audit and report on the types of files open on the file server, my hunch was a certain select number of users were running applications (like *gulp* lotus notes) from the network share.