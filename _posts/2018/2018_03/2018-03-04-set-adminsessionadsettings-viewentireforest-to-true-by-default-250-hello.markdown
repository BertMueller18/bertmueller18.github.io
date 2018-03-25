---
layout: post 
title:  "Set AdminSessionADSettings ViewEntireForest To True By Default – 250  Hello" 
date:   2018-03-04T10:53:34.106Z 
categories: exchange powershell
link: https://blogs.technet.microsoft.com/rmilne/2014/09/08/set-adminsessionadsettings-viewentireforest-to-true-by-default/ 
tags:
  - links
ogtype: article 
---
## 
Set AdminSessionADSettings ViewEntireForest To True By Default

In Exchange 2010 the Set-AdServerSettings  cmdlet is used to manage the AD environment in the current Exchange Management Shell (EMS) session.  In Exchange 2007 there was a variable called AdminSessionADSettings  for the same purpose.  Exchange admins normally use the Set-AdServerSettings cmdlet to change a session’s view scope, so that they can see objects in multiple domains.  By default EMS places the focus on the local domain. 

This can become tedious if we have to change scope at the start of every EMS session. 

This was exactly the question posed during a recent workshop - How to set EMS so that it will default to the forest?