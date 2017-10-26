---
layout: post 
title:  "Windows 10 save start menu layout to XML using PowerShell - Imran Qureshi" 
date:   2017-10-16T20:55:10.526Z 
categories: windows10 deployment
link: https://1iq.uk/windows-10-save-start-menu-layout-xml-using-powershell/?utm_content=buffer5da3d&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer 
tags:
  - links
ogtype: article 
---

> Windows 10 save start menu layout to XML using PowerShell
Published September 16, 2017
OK so finally starting to work this out. I want to save the start menu and taskbar layout to use on a new Windows 10 Image.

The start menu consists of:
Menu, Start layout (tiles) which have pinned folders and dynamic app tiles
Some areas can be managed with GP or MDM Policy.

In Win 10 you can pin apps to taskbar and remove default pinned apps.
3 Categories of pinned apps:
Apps pinned by user, default during OS install, apps pinned by enterprise with unattended setup.
You can specify apps to pin using Application User Model ID (AUMID) or the local path.

The AUMID method shows mainly the Store Apps so I will use the local path method as PowerShell is one of the pinned apps i need.

I want to create a partial start layout which lets me move tile groups and create new groups if required but not edit the existing ones preconfigured.
A full start layout does not let a user pin, unpin or unistall apps from the start menu.

So I pin/unpin the tiles i want in the start layout.

Once ready run the following Cmdlet in PS:
Export-StartLayout -Path "C:\imagestore\StartLayout.xml"

Configure the XML file for partial start layout open it and add this to <DefaultLayoutOverride>:
<DefaultLayoutOverride LayoutCustomizationRestrictionType="OnlySpecifiedGroups">

This can then be added into GP placed on a network share for multiple desktops, imported with Import-StartLayout into a WIM image or added to a WCD Provisioning Package.