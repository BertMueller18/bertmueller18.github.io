---
layout: post 
title:  "IT Support and Migration Notes: Exchange 2013 - Use the Recovery Database to Restore Mailbox or Inbox Rules" 
date:   2017-05-16T21:30:30.059Z 
categories: exchange exchange2013 recovery
tags:
  - links
ogtype: article 
---

## Exchange 2013 - Use the Recovery Database to Restore Mailbox or Inbox Rules
 
Pre requisites
Access to a healthy backup.
Name of the mailbox(es) you want to recover example: ITSupport
Create a temp user with mailbox (IT2)
Access to the exchange server.
 
Procedures and steps
 
1-    Check you have enough space to accommodate the exchange database file that you will copy from the backup
2-    Copy the edb file from the backup and the log files to a folder called Recovery and the logs to a sub-folder Logs
3-    Start the EMS and run
eseutil /mh <the .edb file>
the status will show Dirty Shutdown.
4-    Run the following command to bring the database to clean shutdown state,
eseutil /R Exx /l G:\Recovery\Logs /d G:\Recovery
5-    Create the recovery database
New-MailboxDatabase –Recovery –Name RDB1 –Server <ExchangeServerName> -Edbfilepath G:\Recovery\<the.edb file> -LogFolderPath G:\Recovery\Logs
Restart-Service MSExchangeIS
6-    Mount the database
Mount-Database RDB1
7-    Verify that the mounted database contains the mailbox(es) you want to restore
Get-MailboxStatistics –Database RDB1 | Ft –auto
8-    Start the recovery process
New-MailboxRestoreRequest –SourceDatabase RDB1 –SourceStoreMailbox “ITSupport” –TargetMailbox IT2 –BadItemsLimit 10
9-    You can use the following to monitor the restore process
Get-MailboxRestoreRequest
Get-MailboxRestoreRequest | Get-MailboxRestoreRequestStatistics -IncludeReport |Format-List > C:\AllRestoreReports.txt
 
 
10- Once the restore has a status Completed run
Get-MailboxRestoreRequest –Status Completed | Remove-MailboxRestoreRequest
11- Now you can access the mailbox from your Outlook and you can restore or export any item you want include Inbox Rules just make sure there are no errors in the rules (red text) before you can export it to a file and select the server side when you access the rules.
12- When you finish clean what you did unless you deal with a lot of recovery issues like this. You can remove the Recovery database
Remove-MailboxDatabase –Id RDB1
13- Delete recovery folder and all of its contents.
