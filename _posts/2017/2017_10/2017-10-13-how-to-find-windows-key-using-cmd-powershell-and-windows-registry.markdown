---
layout: post 
title:  "How To Find Windows Key Using CMD, PowerShell, And Windows Registry" 
date:   2017-10-13T13:05:12.020Z 
categories: windows licensing deployment
link: https://fossbytes.com/how-to-find-windows-product-key-lost-cmd-powershell-registry/?utm_content=buffer12f5b&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer 
tags:
  - links
ogtype: article 
---

> How To Find Windows Product Key Using CMD, PowerShell, And Windows Registry
July 26, 2016
SHARE Facebook Twitter  

Short Bytes: If you are willing to reinstall your Windows operating system, it’s possible that you’ll be stuck at some point due to lost Windows key. However, using some simple methods that involve PowerShell, Command Prompt, and Windows Registry, you can easily find Windows product key. These methods are a lifesaver for every Windows user and they just need a couple of steps.

````vbscript
Set WshShell = CreateObject("WScript.Shell")
MsgBox ConvertToKey(WshShell.RegRead("HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\DigitalProductId"))

Function ConvertToKey(Key)
Const KeyOffset = 52
i = 28
Chars = "BCDFGHJKMPQRTVWXY2346789"
Do
Cur = 0
x = 14
Do
Cur = Cur * 256
Cur = Key(x + KeyOffset) + Cur
Key(x + KeyOffset) = (Cur \ 24) And 255
Cur = Cur Mod 24
x = x -1
Loop While x &gt;= 0
i = i -1
KeyOutput = Mid(Chars, Cur + 1, 1) &amp; KeyOutput
If (((29 - i) Mod 6) = 0) And (i &lt;&gt; -1) Then
i = i -1
KeyOutput = "-" &amp; KeyOutput
End If
Loop While i &gt;= 0
ConvertToKey = KeyOutput
End Function
````
### powershell from bios
````powershell “(Get-WmiObject -query ‘select * from SoftwareLicensingService’).OA3xOriginalProductKey”````

````wmic path softwarelicensingservice get OA3xOriginalProductKey````