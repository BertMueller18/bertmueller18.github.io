---
layout: post 
published: true 
title: "Vyacheslav Fedenko: Hyper-V Replica with self-signed certificates" 
date: 2016-06-27T08:25:45.106Z 
link: http://blog.fedenko.info/2016/06/hyper-v-replica-with-self-signed.html 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Hyper-V Replica with self-signed certificates
I have two standalone non-domain joined Hyper-V servers - HV01 and HV02. I need to configure Hyper-V replica between them. Many blog post and guides provide syntax for MakeCert tool. Interesting thing is that MakeCert is deprecated and it is recommended to use New-SelfSignedCertificate cmdlet instead. Of course it is great but there are some limitations of this cmdlet in PowerShell 4.0. Actually there is huge difference between New-SelfSignedCertificate cmdlet in PowerShell 4.0 and 5.0. I will create self-signed certificate using new cmdlet that's why I use Windows 10 with PowerShell 5.0. The name of Windows 10 workstation will be ADMIN01.