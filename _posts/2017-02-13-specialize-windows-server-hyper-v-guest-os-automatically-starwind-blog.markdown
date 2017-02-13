---
layout: post 
title:  "Specialize Windows Server Hyper-V guest OS automatically | StarWind Blog" 
date:   2017-02-13T12:46:26.592Z 
categories: deployment server2016 unattend
link: https://www.starwindsoftware.com/blog/specialize-windows-server-hyper-v-guest-os-automatically 
tags:
  - links
ogtype: article 
---

> Specialize Windows Server Hyper-V guest OS automatically
Posted by Romain Serre on February 6, 2017	
Tags: Active Directory, AD, Hyper-V, PowerShell, VHDX, Virtual Machine, Virtual Machine Manager, VMM, Windows Server
0016100
No ratings yet.
Last year I have written a topic on Starwind to create VMs from PowerShell. That enables to automate the creation process without using a GUI, either from Virtual Machine Manager or Hyper-V Manager. But a VM deployment is not finished when the VM is created but when the application is deployed. Before deploying the application, the OS must also be installed and specialized. This topic shows you the method I use to deploy and specialize a VM without a single click.