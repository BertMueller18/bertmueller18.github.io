---
layout: post 
title:  "Streamlined Migration of FRS to DFSR SYSVOL | Storage at Microsoft" 
date:   2018-07-05T13:02:45.230Z 
categories: activedirectory dfsr migration ntfrs
link: https://blogs.technet.microsoft.com/filecab/2014/06/25/streamlined-migration-of-frs-to-dfsr-sysvol/ 
tags:
  - links
ogtype: article 
---

## Streamlined Migration of FRS to DFSR SYSVOL

June 25, 2014 by NedPyle [MSFT] // 28 Comments
Share
Hi folks, Ned here again. When telling people about the coming removal of FRS from Windows Server, the main response is usually:

“Sure, I have occasional problems with FRS and know that I should upgrade to DFSR, but who has the time for a huge migration? That guide is very intimidating!”

Update June 20, 2017: It is done; Windows Server 2016 RS1 is the last version that will allow FRS – RS3 no longer includes the binaries. https://support.microsoft.com/en-us/help/4025991/windows-server-2016-rs3-no-longer-supports-frs

I hear you on the guide; it is 52 pages of verbosity and completeness. This implies that migration normally takes weeks or months though, which is untrue. With smaller domains, it should take a few minutes, and with larger ones, a few hours or days at most. Migrations are staged, with no interruption to users, and can be rolled back until completed.