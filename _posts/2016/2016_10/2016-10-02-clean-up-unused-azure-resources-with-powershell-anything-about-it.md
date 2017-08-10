---
layout: post 
published: true 
title: "Clean up unused Azure Resources with PowerShell – Anything about IT" 
date: 2016-10-02T11:34:45.940Z 
categories: azure azurerm powershell
link: http://www.verboon.info/2016/10/clean-up-unused-azure-resources-with-powershell/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## Clean up unused Azure Resources with PowerShell
Posted on2 October 2016AuthorAlex VerboonLeave a comment

Today when I opened my Azure portal I had a little surprise. The monthly MSDN subscription credit was much lower as I expected it to be. Did I eventually forget to turn off a virtual machine? Curious to find out where the cost had come from, I drilled into the subscription details and noticed that the higher costs had come from the Premium storage that I had used recently to deploy a virtual machine using an SSD disk  instead of a HDD disk. But still it wasn’t clear why just that one virtual machine would be that expensive, so i drilled into the premier storage account and noticed that there were several orphaned VHD disks there. A clean up was required.

To get an overview of all disks, I wrote the following script called Get-AzureBlobInfo. The script queries all or the specified storage account name and lists all blob objects stored within the containers.

