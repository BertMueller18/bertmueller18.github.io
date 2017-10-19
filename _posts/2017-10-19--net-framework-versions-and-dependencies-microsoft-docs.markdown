---
layout: post 
title:  ".NET Framework Versions and Dependencies | Microsoft Docs" 
date:   2017-10-19T20:26:43.989Z 
categories: deployment dotnet
link: https://docs.microsoft.com/en-us/dotnet/framework/migration-guide/versions-and-dependencies 
tags:
  - links
ogtype: article 
---

## NET Framework Versions and Dependencies
10/17/2017 9 minutes to read Contributors           all
Each version of the .NET Framework contains the common language runtime (CLR), the base class libraries, and other managed libraries. This topic describes the key features of the .NET Framework by version, provides information about the underlying CLR versions and associated development environments, and identifies the versions that are installed by the Windows operating system.
Note
For information on downloading and installing the .NET Framework, see Install the .NET Framework for developers.
The following table summarizes .NET Framework version history and correlates each version with Visual Studio, Windows, and Windows Server. Note that Visual Studio provides multi-targeting, so you are not limited to the version of the .NET Framework that is listed.
Each new version of the .NET Framework retains features from the previous versions and adds new features. The CLR is identified by its own version number. The .NET Framework version number is incremented at each release, although the CLR version is not always incremented. For example, the .NET Framework 4, 4.5, and later releases include CLR 4, but the .NET Framework 2.0, 3.0, and 3.5 include CLR 2.0. (There was no version 3 of the CLR.)
See System Requirements for a complete list of supported operating systems. For downloads, see Install the .NET Framework for developers. For determining which versions of the .NET Framework are installed on a computer, see How to: Determine Which .NET Framework Versions Are Installed.
In the table, versions of the .NET Framework that are installed on operating system versions marked with ✓ in the Included in/Can be installed on Windows and the Included in/Can be installed on Windows Server columns must be enabled in Control Panel (for Windows) or enabled through the Server Manager (for Windows Server).