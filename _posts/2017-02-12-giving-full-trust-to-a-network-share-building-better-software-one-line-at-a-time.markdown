---
layout: post 
title:  "Giving full trust to a network share – Building Better Software – One Line At A Time" 
date:   2017-02-12T18:48:27.271Z 
categories: security powershell winrm
link: https://blogs.msdn.microsoft.com/permanenttan/2008/06/05/giving-full-trust-to-a-network-share/ 
tags:
  - links
ogtype: article 
---

## Giving full trust to a network share
★★★★★★★★★★★★★★★

I work on multiple machines and, very often, I need access to my tool sets on each machine that I work on. This is accomplished by sharing out my tools folder/drive and restrict full permissions to myself. There is a little wrinkle. Network shares by default only get LocalIntranet permissions and that may not be sufficient for some exes and managed assemblies. Fortunately there is the tool “caspol.exe” (normally located in the installed .NET framework folder, \Windows\Microsoft.NET\Framework\vN.N.NNNNN\CasPol.exe). caspol.exe can tell the client computer to give full trust to a network share which in turn enables the execution of exes and loading of assemblies directly from the network share.


Here is how I give full trust to a network share //MyDevBox/MyTools:


caspol.exe  -m  -ag 1.2  -url file://MyDevBox/MyTools/*  FullTrust


Giving full trust is also needed if you share development of Visual Studio projects/solutions across different machines. For example, I would develop code on my dev box and run test on multiple VPCs with the sources/binaries shared with full trust.


Hope this helps.