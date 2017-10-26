---
layout: post 
title:  "Windows PowerShell and DSC on Linux in Microsoft Azure | Ask  Premier Field Engineering (PFE)  Platforms" 
date:   2017-10-16T20:57:20.205Z 
categories: powershell psdsc linux
link: https://blogs.technet.microsoft.com/askpfeplat/2017/10/16/windows-powershell-and-dsc-on-linux-in-microsoft-azure/?utm_source=dlvr.it&utm_medium=twitter 
tags:
  - links
ogtype: article 
---

## Windows PowerShell and DSC on Linux in Microsoft Azure

October 16, 2017 by BrandonWilson // 0 Comments

Hello everyone! I’m Preston K. Parsard, Platforms PFE and I’d like to talk about running PowerShell and Desired State Configuration (DSC) on Linux in Microsoft Azure. Just in case you haven’t heard yet, PowerShell has been open sourced and released for Linux since 18 August, 2016. More details and other resources for the announcement can be found here. If you are new to DSC in general, you may want to first hop over to one of the posts my colleage Dan Cuomo wrote about for a quick intro and a plethora of online training resources here, then pop back to this post and continue reading.

What challenges does this address?

Different operating system platforms requires different tools, standards and procedures, and in many cases, multiple teams of IT Pros. This requires more resources and can create silos within the IT department. DevOps aims to enhance business value by improving operations for people, proceses and technology by encouraging cross-platform collaboration and integration to simplify IT operations.

What are the benefits?

For teams with Windows administrators in a predominantly Windows environment, who manage a few Linux systems, or Linux administrators in a largely Linux shops that must also administer some Windows machines; Both may now realize the benefit of leveraging a single set of tools and standards such as PowerShell and DSC.

1.    Efficiency: With this script, you can now quickly create a basic test environment infrastructure in as little as about 30 minutes, to begin explore the features of PowerShell and DSC on Linux.

2.    Cost: There is no capital investment required to set up storage, networking, compute, a home lab, or a physical facility since this is all done in Azure. An Azure subscription is required though, which you can try it free for 30 days here.

3.    Administration: The administrative requirements to create this environment is much lower than managing physical infrastructure directly, and the complexity of the setup is handled automatically in the code.

4.    Training & Skills Development: PowerShell and DSC on Linux is still a fairly new concept, but now you can review this post and use the script to reference how it works in detail, sort of like the “Infrastructure as Code” idea to develop these cross-platform skills. You may even decide later to contribute back to the PowerShell Core community to make things better and easier for all of us in the spirit of collaboration and continuous improvement.

As an IT Pro, knowledge of a widely accepted technology implemented across multiple platforms means you can also offer and demonstrate more valuable skills for your current or future employers, plus it’s just more fun anyway!