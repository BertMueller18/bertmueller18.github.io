---
layout: post 
title:  "Configuring NTP with Master Clock in Isolated Network - CareExchange.in" 
date:   2017-05-07T21:56:18.792Z 
categories: activedirectory ntp networking 
link: http://www.careexchange.in/configuring-ntp-with-master-clock-in-isolated-network/ 
tags:
  - links
ogtype: article 
---

> Configuring NTP with Master Clock in Isolated Network
2 weeks ago	Active Directory, VMware, Windows Server

Typically in Active Directory Based Environment – Primary Domain Controller (PDC) will be the master for Time and all other domain joined machines will receive time from the master.

Login to Primary Domain Controller (PDC) which holds PDC Emulator Role – In my Case its an Windows Server 2012 R2 or above.

To Find who is holding the PDC Role – Login to Active Directory –