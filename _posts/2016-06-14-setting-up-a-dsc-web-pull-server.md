---
layout: post 
published: true 
title: "Setting up a DSC web pull server" 
date: 2016-06-14T12:42:06.358Z 
link: https://msdn.microsoft.com/en-us/powershell/dsc/pullserver?f=255&MSPPError=-2147217396 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Setting up a DSC web pull server

Eric Slesar|Last Updated: 5/27/2016|8 Contributors
Applies To: Windows PowerShell 5.0
A DSC web pull server is a web service in IIS that uses an OData interface to make DSC configuration files available to target nodes when those nodes ask for them.

Requirements for using a pull server:

A server running:
WMF/PowerShell 5.0 or greater
IIS server role
DSC Service
Ideally, some means of generating a certificate, to secure credentials passed to the Local Configuration Manager (LCM) on target nodes
You can add the IIS server role and DSC Service with the Add Roles and Features wizard in Server Manager, or by using PowerShell. The sample scripts included in this topic will handle both of these steps for you as well.