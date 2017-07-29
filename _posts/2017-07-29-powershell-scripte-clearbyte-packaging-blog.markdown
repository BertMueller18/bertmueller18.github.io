---
layout: post 
title:  "Powershell Scripte | clearByte Packaging Blog" 
date:   2017-07-29T21:25:53.022Z 
categories: powershell automation
link: http://blog.clearbyte.ch/powershell-scripte/ 
tags:
  - links
ogtype: article 
---

> POWERSHELL SCRIPTE
Dezember 2015 | Adriano Parrella

Hier stelle ich Euch zwei, drei Powershell Scripte zur Verfügung, welche bei diversen Gelegenheiten eingesetzt habe. Die Scripts müssen selbstverständlich für Eure Bedürfnisse angepasst, und im LAB getestet werden!
Welche Patches sind auf dem Client Installiert?

### Windows  Updates
````powershell
$UpdateSession = New-Object -ComObject Microsoft.Update.Session
$SearchResult = $null
$UpdateSearcher = $UpdateSession.CreateUpdateSearcher()
$UpdateSearcher.Online = $true
$SearchResult = $UpdateSearcher.Search("IsInstalled=1 and Type='Software'")
$i = 1
foreach($Update in $SearchResult.Updates) {
······ Write-Output "$i) $($Update.Title + " , KB" +$Update.KBArticleIDs + " , " + $Update.SecurityBulletinIDs)" | Out-File -Filepath "C:\temp\test.csv"· -Append
······ $i += 1
}
````
### Auslesen der Mac Adressen
````powershell
Get-NetAdapter | select Name,MacAddress
````
###Auslesen der UUID
````powershell
Get-WmiObject -Class Win32_ComputerSystemProduct | Select-Object -Property UUID
````
#### Auslesen der MAC Adressen
````powershell
Get-WmiObject win32_networkadapterconfiguration | select description, macaddress
````
### Messagebox im LoginScript?
````powershell
$OUTPUT=[System.Windows.Forms.MessageBox]::Show("Bitte warten Sie... es muss das etwas angepasst werden." , "Status" , 0)
if ($OUTPUT -eq "OK"){
   Write-Host "ok"
} else {
   Write-Host "abort"
}
````
### Eine Funktion, welche wartet bis Notepad gestartet ist
````powershell
Function Wait-For-Explorer {
   $process = 'notepad.exe'
   $waitTime = 1
   While ($owner.User -ne $env:USERNAME) {
      try
   {
      $owner = (Get-WmiObject -class win32_process | where { $_.ProcessName -eq $process }).GetOwner() | Select -Property User
   } catch {
      Write-Host "Zzzzz...."
      Start-Sleep -Seconds $waitTime
   }
}
Write-Host "Process ${process} is running..."
````