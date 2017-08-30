---
layout: post 
title:  "PC Tech Go: Faster Active Directory Replication - Decrease Intersite Replication Interval to Seconds" 
date:   2017-08-23T00:01:45.610Z 
categories: activedirectory replication
link: http://pctechgo.blogspot.de/2014/03/active-directory-intersite-replication.html 
tags:
  - links
ogtype: article 
---


## Faster Active Directory Replication - Decrease Intersite Replication Interval to Seconds

### Enable Fast Domain Controller Replication

Active Directory Intersite Replication Interval Enable Faster AD and DNS updates  

Enable Faster Active Directory AD and DNS Replication Updates Between Sites 

Although for some newer administrators making changes to Active Directory could be a nerve rattling proposition, making this change to speed up active directory replication can only be accomplished using this method. Using the standard GUI Microsoft Management Consoles to make the change to speed up Active Directory replication is not possible. The best result of using administrator consoles will be to increase domain replication between domain controllers to 15 minutes. These large time values were instituted into Active Directory at version 1 because inter-site connections during that era of computing and networking were much lower in bandwidth with the most common being frame-relay or 56k circuits. Since then, inter-site connections and the Internet speeds have increased tremendously so faster domain controller replication is possible even over wan links. 