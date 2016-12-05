---
layout: post 
title:  "How To Request Certificate Without Using IIS or Exchange – 250  Hello" 
date:   2016-12-05T10:01:48.282Z 
categories: pki certificate certreq
link: https://blogs.technet.microsoft.com/rmilne/2014/06/17/how-to-request-certificate-without-using-iis-or-exchange/ 
tags:
  - links
ogtype: article 
---

#How To Request Certificate Without Using IIS or Exchange

The blog post on how to integrate Office 365 with Windows 2012 R2 AD FS raised an interesting question from a reader (Hi Eric!) on how should he request a certificate for the AD FS instance since there is no longer an IIS dependency.  This means that there is no longer an IIS console to generate a certificate request with.  What to do?

You could generate a certificate request, complete it and then export it to a .pfx file on an Exchange server.  The exported certificate can then be copied over to the AD FS server[s] and then imported to the local computer certificate store to make it available for AD FS purposes.

What if you don’t want, or can’t do this?  If you want to do this on the AD FS server directly then certreq.exe can help us out here!  This also applies to other servers and the application of the steps here are not just for AD FS.  However the question raised means that more folks in the field are probably thinking about the same thing, so that forced me to polish off yet another one of those draft blog posts!

 