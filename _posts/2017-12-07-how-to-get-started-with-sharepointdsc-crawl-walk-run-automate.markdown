---
layout: post 
title:  "How to Get Started with SharePointDSC – Crawl, Walk, Run, Automate" 
date:   2017-12-07T07:52:09.900Z 
categories: powershell psdsc sharepoint
link: http://nikcharlebois.com/how-to-get-started-with-sharepointdsc/ 
tags:
  - links
ogtype: article 
---

> How to Get Started with SharePointDSC
 2017-07-28  Nik Charlebois	 Tutorial  828 12 Comments
The goal of this article is to help people interested in learning how to use PowerShell Desired State Configuration (DSC) to configure their SharePoint environment get started. While it is totally possible for you to configure a SharePoint Farm on an environment that has PowerShell 4.0 installed on, it is our recommendation that you try to use PowerShell 5+ as much as possible, as it offers a lot of improvements on the DSC side. The example covered in this article will be a Single Server SharePoint 2016 farm deployed with SQL Server 2016, on Windows Server 2016. We will be using DSC in push mode, meaning that we will manually execute the Start-DSCConfiguration cmdlet on the environment, and will ensure all dependent DSC Modules are put on the server prior to attempting to configure it.

The end-goal for this article, is to have a brand new Windows Server 2016 virtual machine with nothing on it to begin with, and then let DSC do the following automatically: