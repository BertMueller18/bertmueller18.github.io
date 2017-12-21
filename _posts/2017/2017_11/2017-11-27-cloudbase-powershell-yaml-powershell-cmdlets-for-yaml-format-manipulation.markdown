---
layout: post 
title:  "cloudbase/powershell-yaml: PowerShell CmdLets for YAML format manipulation" 
date:   2017-11-27T10:03:40.180Z 
categories: powershell yaml programming
link: https://github.com/cloudbase/powershell-yaml 
tags:
  - links
ogtype: article 
---

## powershell-yaml

This powershell module is a thin wrapper on top of YamlDotNet that serializes and un-serializes simple powershell objects to and from YAML. It was tested on powershell versions 4 and 5, supports Nano Server and aparently works with powershell on Linux. I suspect it works on Mac as well, but I have not had a chance to test it.

The lib folder contains the YamlDotNet assemblies. They are not really required, just a fall-back in case your system does not already have them installed and loaded. Feel free to remove the lib folder if you prefer to add the required assemblies yourself.