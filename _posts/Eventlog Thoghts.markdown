
## get-winevent Examples
### Explore the unique events in an event log, including examples
Get-WinEvent Application | group Id | ft -w {$_.Name},{$_.Group[0].Message}

Get-WinEvent -FilterHashTable @{ LogName = 'System'; ID= 36888 } -ComputerName <server>

### Forensics: Automating Active Directory Account Lockout Search with PowerShell (an example of deep XML filtering of event logs across multiple servers in parallel)
(https://blogs.technet.microsoft.com/ashleymcglone/2015/08/31/forensics-automating-active-directory-account-lockout-search-with-powershell-an-example-of-deep-xml-filtering-of-event-logs-across-multiple-servers-in-parallel/
)

### Search the event log with the Get-WinEvent PowerShell cmdlet
(https://4sysops.com/archives/search-the-event-log-with-the-get-winevent-powershell-cmdlet/)

