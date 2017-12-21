---
layout: post 
title:  "Deploying a Multi-Server SharePoint Farm with PowerShell Desired State Configuration – Crawl, Walk, Run, Automate" 
date:   2017-12-07T07:55:18.902Z 
categories:  powershell psdsc automation sharepoint
link: http://nikcharlebois.com/deploying-a-multi-server-sharepoint-farm-with-powershell-desired-state-configuration/ 
tags:
  - links
ogtype: article 
---

## Deploying a Multi-Server SharePoint Farm with PowerShell Desired State Configuration

>2017-03-31  Nik Charlebois	 Tutorial  455 5 Comments

In this article we will cover the process of writing a DSC Configuration with SharePointDSC and deploying it to multiple servers to create a SharePoint 2016 farm (note that this would also work for SharePoint 2013 with minor changes to the SPFarm block). We will be using a Push Refresh mode, meaning that the Configuration will be manually applied to our servers, and not using a Pull Server to centrally manage the configuration. Using this approach, if our configuration was to change, it would need to be manually re-pushed onto the servers in the farm. While I believe that in most cases, you will wish to use a Pull refresh mode along with an Enterprise Pull Server to manage your SharePoint deployments, we are using a Push mode to keep things simple for the sake of this article.

The article will cover a scenario I will be demonstrating over at SPTechCon Austin next week. In this demo, I have a very small multi-server SharePoint 2016 farm that is made up of one dedicated SQL Server 2016 (SPTechCon-SQL), one Web Front-End (SPTechCon-WFE1), and one Application Server (SPTechCon-APP1). The configuration script will be built on a separate machine named (SPTechCon-Pull) and will be remotely applied to the servers in my farm from that machine. The figure below gives you a complete overview of the landscape of my demo.

