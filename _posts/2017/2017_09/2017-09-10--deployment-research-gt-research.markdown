---
layout: post 
title:  "	Deployment Research &gt; Research" 
date:   2017-09-10T17:44:37.234Z 
categories: deployment winpe netmon automation
link: https://deploymentresearch.com/Research/Post/647/How-to-run-Microsoft-Network-Monitor-in-WinPE 
tags:
  - links
ogtype: article 
---

In this guide you learn how to run the Microsoft Network Monitor in WinPE, for example for advanced debugging of OS Deployment issues. This guide is based on the following KB article from Microsoft: https://support.microsoft.com/en-us/help/4034393/how-to-get-network-captures-from-a-task-sequence-in-windows-pe. But I’ve added some clarification steps, as well as PowerShell scripts to make the process easier (and automated).

To run Microsoft Network Monitor in WinPE you basically have to do three things:

Extract the Network Monitor files
Add the Network Monitor files, and driver, to WinPE
Start Network Monitor after WinPE has booted
