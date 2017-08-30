---
layout: post 
title:  "Trigger an Active Directory replication with PowerShell - It for DummiesIt for Dummies" 
date:   2017-08-07T08:51:57.720Z 
categories: activedirectory replication
link: https://itfordummies.net/2014/11/05/trigger-active-directory-replication-powershell/ 
tags:
  - links
ogtype: article 
---

## Trigger an Active Directory replication with PowerShell
Posted on November 5, 2014 by edemilliere
Hello,

Many of us already use “RepAdmin /SyncAll” to force an Active Directory replication.You can emulate that with those PowerShell lines :

[System.DirectoryServices.ActiveDirectory.Domain]::GetCurrentDomain().DomainControllers | % {
    $_.SyncReplicaFromAllServers("DC=D2K12R2,DC=local",'CrossSite')
}
The ‘CrossSite’ parameter is a “System.DirectoryServices.ActiveDirectory.SyncFromAllServersOptions“, you can see the possible options with :

[Enum]::GetValues("System.DirectoryServices.ActiveDirectory.SyncFromAllServersOptions")
The first parameter of the “SyncReplicaFromAllServers” method, is the distinguished name of the naming context you want to trigger replication.