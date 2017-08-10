
## get-winevent Examples
### Explore the unique events in an event log, including examples
````powershell
Get-WinEvent Application | group Id | ft -w {$_.Name},{$_.Group[0].Message}

Get-WinEvent -FilterHashTable @{ LogName = 'System'; ID= 36888 } -ComputerName <server>
````
### Forensics: Automating Active Directory Account Lockout Search with PowerShell (an example of deep XML filtering of event logs across multiple servers in parallel)
(https://blogs.technet.microsoft.com/ashleymcglone/2015/08/31/forensics-automating-active-directory-account-lockout-search-with-powershell-an-example-of-deep-xml-filtering-of-event-logs-across-multiple-servers-in-parallel/
)

### Search the event log with the Get-WinEvent PowerShell cmdlet
(https://4sysops.com/archives/search-the-event-log-with-the-get-winevent-powershell-cmdlet/)
### Windows Log Hunting with PowerShell
(http://909research.com/windows-log-hunting-with-powershell/)

All windows security log event IDs, ranked by least frequent: 

````Get-WinEvent -FilterHashtable @{logname="security"}| Group-Object id -NoElement | sort count````

All usernames who have logged in: 

````Get-WinEvent -FilterHashtable @{logname="security";id=4624} | %{$_.Properties[5].Value} | sort -Unique````

Count of logins by username: 

````Get-WinEvent -FilterHashtable @{logname="security";id=4624} | %{$_.Properties[5].Value} | group-object -noelement | sort count````

All domains for accounts that have logged in: 

````Get-WinEvent -FilterHashtable @{logname="security";id=4624} | %{$_.Properties[6].Value} | sort -Unique````

SIDs for all accounts that have logged in: 

````Get-WinEvent -FilterHashtable @{logname="security";id=4624} | %{$_.Properties[4].Value} | sort -Unique````

Failed login count by username: 

````Get-WinEvent -FilterHashtable @{logname="security";id=4625} | %{$_.Properties[1].Value} | Group-Object -noelement````

Invalid usernames used for login attempts (looking for account guessing) 

````Get-WinEvent -FilterHashtable @{logname="security";id=4776} | %{$_.Properties[1].Value} | sort -Unique````

AppLocker events - List all executables and scripts that were against policy.
Use event ID 8003/8004 (audit mode/block mode) for exe and dll files: 

````Get-WinEvent -FilterHashtable @{logname="Microsoft-Windows-AppLocker/EXE and DLL";id=8003} | select message```` 
Use event ID 8006/8007 for script or MSI files: ````Get-WinEvent -FilterHashtable @{logname="Microsoft-Windows-AppLocker/MSI and Script";id=8006} | select message````
