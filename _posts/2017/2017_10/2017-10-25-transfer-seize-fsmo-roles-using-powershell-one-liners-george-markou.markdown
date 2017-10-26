---
layout: post 
title:  "Transfer/Seize FSMO Roles using Powershell ( one-liners ) - George Markou" 
date:   2017-10-25T14:29:08.765Z 
categories: activedirectory fsmo
link: http://www.markou.me/2017/10/transferseize-fsmo-roles-using-powershell-one-liners/ 
tags:
  - links
ogtype: article 
---

> Transfer/Seize FSMO Roles using Powershell ( one-liners )
Written by George Markou 
 ActiveDirectory, Powershell, Scripts, Server, Windows	 Windows Server  Leave a Comment 
The following one-liner PowerShell cmdlets will allow you to Transfer the FSMO Roles or Seize them in case of a faulty and permanently offline Domain Controller.

Execute the following cmdlets using from an elevated PowerShell Prompt.


1
2
3
4
5
6
7
8
#Transfer a single FSMO Role (PDCEmulator in this example)
Move-ADDirectoryServerOperationMasterRole -Identity "Target-DC" -OperationMasterRole PDCEmulator
 
#Transfer all FSMO Roles
Move-ADDirectoryServerOperationMasterRole -Identity "Target-DC" -OperationMasterRole SchemaMaster, DomainNamingMaster, InfrastructureMaster, PDCEmulator, RIDMaster
 
#Seizing all FSMO Roles from a Faulty or Permanently Offline Domain Controller
Move-ADDirectoryServerOperationMasterRole -Identity "Target-DC" -OperationMasterRole SchemaMaster, DomainNamingMaster, InfrastructureMaster, PDCEmulator, RIDMaster -Force
Thanks for reading!