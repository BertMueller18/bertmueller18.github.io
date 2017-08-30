---
layout: post 
title:  "How to Configure Fast Cached Exchange Mode Settings for Outlook 2010 and Outlook 2013 Using Group Policy | The EXPTA {blog}" 
date:   2017-08-25T13:21:48.847Z 
categories: exchange outlookanywhere outlook
link: http://www.expta.com/2010/10/how-to-configure-fast-cached-exchange.html 
tags:
  - links
ogtype: article 
---

## How to Configure Fast Cached Exchange Mode Settings for Outlook 2010 and Outlook 2013 Using Group Policy
Saturday, October 30, 2010
Note: This article and included ADM and REG files have been updated to work with Outlook 2013, as well as Outlook 2010.

Microsoft introduced Cached Exchange Mode in Outlook 2003 and it's been the default configuration ever since.  Cached Exchange Mode saves a copy of your mailbox on your computer which provides quick access to your data and is frequently updated with the Exchange server.



Cached Exchange Mode works like this: When the Exchange Server notifies Outlook of a change, the Download timer starts and Outlook delays receiving the change information.  All notifications that occur in the 30 second window of the Download timer are grouped and processed as a batch at the end of the timer, then the timer is reset.  Uploads to Exchange use a similar Upload timer, which lasts 15 seconds.  For more information, see Description of Outlook 2003 with Cached Exchange Mode in an Exchange Server 2003 environment.  This behavior is the same in Outlook 2007, Outlook 2010, and Outlook 2013.

While this configuration reduces network utilization and load on the target Exchange servers, it reduces the "perceived" performance of Outlook/Exchange.  Users who change from Online Mode to Cached Exchange Mode frequently complain about slow performance, since they're used to the almost "instant messaging" behavior of Online Mode.

This behavior can be changed using a simple registry change, or, as I recommend, using Group Policy.  By changing the Download, Upload, and Maximum timers to one second, your users will enjoy much improved email performance and you will still see improved network performance over traditional MAPI "Online Mode".
