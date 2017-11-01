---
layout: post 
title:  "Opening A Remote Exchange Management Shell – Working Sysadmin" 
date:   2017-10-31T09:58:47.956Z 
categories: powershell exchange
link: http://www.workingsysadmin.com/opening-a-remote-exchange-management-shell/ 
tags:
  - links
ogtype: article 
---

## Opening A Remote Exchange Management Shell
January 21, 2015Exchange, PowerShell, PowerShell ISEexchange, powershell, powershell ise
Here’s a function I stuck in my PowerShell profile. I found myself making lots of remote connections to my Exchange 2013 environment so I put together a quick function to create the connection for me. It’s far from perfect but it saves me time every single time I use it so check it out.
````powershell
function gimme-exchange ()
{
    $arrExchangeServersURI = @("http://fqdn-of-server-one/Powershell","http://fqdn-of-server-two/Powershell")
    $success = $false
    $UserCredential = Get-Credential
    ForEach ($connectionURI in $arrExchangeServersURI)
    {
        Try
        {
            If($success -ne $true)
            {
                $getMBXconn = new-pssession -configurationname Microsoft.Exchange -connectionuri $connectionURI -Authentication Kerberos -Credential $UserCredential
                $null = Import-PSSession -AllowClobber $getMBXConn
                $success = $true
            }
        }
        catch [Exception]
        {
            $strError = $_.Exception.Message
            $strError = "Error: ${strError}"
            $success = $false
        }
    }
}
````