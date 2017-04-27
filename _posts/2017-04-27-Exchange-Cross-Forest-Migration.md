---
layout: post 
title:  "Exchange Cross Forest Migration Annotations" 
date:   2017-04-27T16:44
categories: exchange migration crossforest activedirectory
link: http://bertmueller18.github.io/
tags:
  - links
ogtype: article 
---
## [Exchange 2010 Cross-Forest Migration Step by Step Guide – Part I](https://blogs.technet.microsoft.com/meamcs/2011/06/10/exchange-2010-cross-forest-migration-step-by-step-guide-part-i/)
This Guide will explain the detailed steps required to do cross forest migration from source forest running Exchange 2003 to target forest running Exchange 2010.

Active Directory Migration Tool (ADMT) will be used to migrate user accounts as well as computer accounts. There are two scenarios when using ADMT to migrate user accounts with Exchange


## [Exchange 2010 Cross-Forest Migration Step by Step Guide – Part II](https://blogs.technet.microsoft.com/meamcs/2011/10/25/exchange-2010-cross-forest-migration-step-by-step-guide-part-ii/)

In Part I of this guide I’ve explained the process of cross-forest migration and the differences between using ADMT first or using Prepare-MoveReuqest.Ps1 script first, I’ve also explained the migration scenario and the current environment.

Starting from this part we will talk about migration challenges and the best way to address these challenges.

## [Exchange 2010, 2013, 2016 Cross Forest Remote PowerShell](https://markgossa.blogspot.de/2015/10/exchange-2010-2013-cross-forest-remote-powershell.html)
If you are attempting a remote PowerShell connection to an Exchange server cross forest (no forest trust) using the method here, you will get the below error:

Connecting to remote server [server] failed with the following error message: WinRM cannot process the request. The following error with errorcode 0x80090311 occurred while using Kerberos authentication: There are currently no logon servers available to service the logon request.
 
## [Cross Forest E2K3 to 2010 Mailbox Migration with linked Mailboxes](http://msexchangeguru.com/2011/08/29/migration/)

I couldn’t find a proper document on performing a cross forest mailbox migration, so here we go…

This document has following assumptions:

Source and Target forest have one way trust
All CAS, HT and MBX servers are installed
All certificated are installed
Send and Receive connectors are configured
Accepted domain and email address policy is configured.
Disclaimer and any other exchange compliance or security rule configured.
Antivirus and antispam are installed and configured.
All the required ports are open between Exchange 2003 server to Exchange 2010 server
Post migration users and mailboxes will be in a separate resource and exchange forest environment.

## [Exchange 2013: Cross Forest/ORG Migration from Exchange 2010/2007](http://msexchangeguru.com/2013/11/03/e2013crossforestmigration/)
Cross forest migration steps blog was long time due from us. So here we go!

Cross forest has changed little bit and requires 3rd party cert in the source domain. 
Some related blogs which can be useful before doing cross forest migration:
Exchange 2013 Design Guide – (http://msexchangeguru.com/2013/07/30/exchange-2013-planning-and-design-guide/)
Exchange 2013 Migration Guide – (http://msexchangeguru.com/2013/05/10/exchange2013-migration/)
Cross Forest E2K3 to 2010 Mailbox Migration with Linked Mailboxes – (http://msexchangeguru.com/2011/08/29/migration/)
Exchange 2013 PF Migration Guide – (http://msexchangeguru.com/2013/04/18/exchange2013-public-folders/)

### This document has following assumptions:

Source and Target forest have a one or 2 way forest trust. This is optional.
All CAS, HT and MBX servers are installed in both the forests.
All certificated are installed.
Send and Receive connectors are configured
Accepted domain and email address policy is configured.
Disclaimer and any other exchange compliance or security rule configured.
Antivirus and antispam are installed and configured.
All the required ports are open between Exchange 2010 server and DCs to Exchange 2013 server and DCs
All CAS and transport configuration completed with the help of Migration Guide
All DAG and Database configuration complete with the help of Migration Guide
All MX, CAS and autodiscover public and AD dns records are configured.
[I'm an inline-style link](https://www.google.com)