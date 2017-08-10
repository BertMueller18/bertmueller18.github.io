---
layout: post 
title:  "Configuring an HTTPS Pull Server for Desired State Configuration PowerShell Version 5" 
date:   2017-03-14T21:50:33.348Z 
categories: psdsc programming deployment powershell
link: http://duffney.io/Configure-HTTPS-DSC-PullServerPSv5 
tags:
  - links
ogtype: article 
---

> Configuring an HTTPS Pull Server for Desired State Configuration PowerShell Version 5
Applies to: Windows PowerShell 5.0
In a previous blog post I walked through the setup of an HTTPS pull server, at the time of the writing there was only one way to setup a pull server with HTTPS. Since that blog post was published, Microsoft has released another version of the Pull server which I’ll refer to as version 2. The offical Microsoft documentation for setting up a pull server can be found here. There are a few key differences between version 1 and version 2. First off, there is no longer a compliance server. Secondly, you now use a registration key to connect to the pull server instead of a configuration ID. A third difference is you can now call out which configurations a node should request from the pull server by name. You no longer have to rename the .mof documents on the pull server with the GUI used for the configuration ID. Keep in mind that both methods still work, however the new method does make combining