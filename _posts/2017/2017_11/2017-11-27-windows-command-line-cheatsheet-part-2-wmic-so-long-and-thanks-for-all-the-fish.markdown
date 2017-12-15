---
layout: post 
title:  "Windows Command Line cheatsheet (part 2): WMIC – So Long, and Thanks for All the Fish" 
date:   2017-11-27T07:27:24.205Z 
categories: pentest wmi windows
link: https://andreafortuna.org/dfir/windows-command-line-cheatsheet-part-2-wmic/amp/ 
tags:
  - links
ogtype: article 
---

## Windows Command Line cheatsheet (part 2): WMIC

Andrea Fortuna
4 months ago
This command-line tool is really useful for both penetration testing and forensics tasks

The previous article has raised interest in readers regarding WMIC.
So I decided to write an article dedicated to this tool.

If you’ve done any scripting for the Windows platform, you’ve probably bumped into the Windows Management Instrumentation (WMI) scripting API, which can be used to enumerate all kinds of information.

The WMIC command-line tool is basically another front-end to access the WMI framework, with the added bonus that numerous queries are pre-defined.
The pre-defined queries mean that you won’t necessarily need to spend any time learning the WMI Query Language (WQL), which is syntactically similar to SQL.

WMIC is included in the default installation of Windows XP (excluding Home edition) and Windows Server 2003. Although WMIC is not included on Windows 2000, you can still usea Windows XP or Server 2003 client to remotely query Windows 2000 systems and receive similar results.

The first time you run WMIC you’ll see a message that WMIC is beinginstalled, but no media is required for installation, nor will anything appear in the Add/Remove Programs list.