---
layout: post 
published: true 
title: "Node.js on Nano Server | Nano Server" 
date: 2016-05-19T22:13:51.564Z 
link: https://blogs.technet.microsoft.com/nanoserver/2016/05/04/node-js-on-nano-server/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Node.js on Nano Server
★★★★★★★★★★★★★★★
May 4, 2016By Refaat Issa [MSFT]0

One of Nano Server’s core scenarios is to serve as a lightweight OS for born-in-the-cloud applications running in a VM or a container. Nano Server already supports ASP.NET Core (aka ASP.NET 5) with IIS, and now, we’re happy to announce support for Node.js.

The instructions in this blog explain how to get Node.js running on Nano Server. If you want to try this on a Nano Server VM, with Windows Server 2016 Technical Preview 5 there are three ways you can quickly get a VM:

Download the developer VHD at the above Technical Preview 5 link
Create a VM in Azure using the Nano Server image in the Azure Gallery. If you don’t have an Azure account, you can get a free 30-day trial
Download the Technical Preview 5 ISO at the above link and then consult the Nano Server documentation to build a VM.
 

Installing Node.js on Nano Server

Download Node.js to your development machine from nodejs.org (I downloaded the LTS version) and follow the installation instructions to install Node.js.

Once installed, use the following PowerShell script from an elevated PowerShell console, classic or ISE, to copy the binaries to your Nano Server machine:

$ip = “0.0.0.0” # the IP address of your Nano Server machine

$s = New-PSSession -ComputerName $ip -Credential ~\Administrator

$nodePath = “C:\Program Files\nodejs”

# this is the default node.js folder – change it if you specified a different folder during installation

Copy-Item -ToSession $s -Path $nodePath -Destination “C:\” -Force -Recurse

 