---
layout: post 
title:  "jaroslad - Addressing the “|” separator problem for virtual FTP Sites (FTP 7.5)." 
date:   2017-03-13T10:31:56.626Z 
categories: iis ftp server2016 windows
link: https://blogs.iis.net/jaroslad/addressing-the-separator-problem-for-virtual-ftp-sites-ftp-7-5 
tags:
  - links
ogtype: article 
---

> Addressing the “|” separator problem for virtual FTP Sites (FTP 7.5).

Thursday, April 16, 2009
FTP 7.0 introduced support for virtual host names as documented in the article http://learn.iis.net/page.aspx/320/using-ftp-virtual-host-names/. Because of variety of compatibility challenges, the decision was made to use the pipe sign “|” as a separator between the virtual host name and the actual account name. To connect to an ftp site configured with virtual host name such as ftp.contoso.com, that was sharing port 21 with some other site, one would need to type ftp.contoso.com|ftpuser to log on successfully.

Pipe sign was intended to address compatibility challenges, but while addressing some, it created new ones as well. One victim of the “I” separator is “Microsoft Expression Web 2” which has a built-in support for FTP publishing. The “|” separator confuses it's credential manager, since it considers it an invalid character which then in turn makes it impossible to connect to virtual FTP site.

To address the issue of “Microsoft Expression Web 2” and possibly other clients that treat “|” in a special way, the updated version of FTP, the FTP 7.5 now allows the administrator to select a new mode of dealing with ftp host names included in the user name.

There is a new configuration setting called useDomainNameAsHostName. What does it do? Just as name suggests, it changes the way how FTP server interprets domain names specified in user name. Microsoft FTP servers has always supported fully qualified user names in the form of

DomainName\user
ComputerName\user
user@DomainName
Often times, it is not required or is not necessary for user to specify the domain name.  If that is the case, then why not to use the familiar syntax to communicate the hostname of the ftp site as if it was a domain name (though it would not be used for the actual windows logon)? That is exactly what FTP 7.5 allows administrator to configure.

If you configure your FTP 7.5 server to allow useDomainNameAsHostName, then it is possible for user to type the virtual host name in the following form

ftp.contoso.com\ftpuser
ftpuser@ftp.contoso.com
It looks more elegant than the original approach with "|" character, doesn’t it? And it also should be easier to use by many ("|" character should really be reserved for use only by geeks). Not to mention that this will make "Microsoft Expression Web 2" and likely handful of other clients work better.

Notes

When useDomainNameAsHostName is set to true, it is still possible to use “I” separator.
If machine’s default domain of the machine is not the one to be used for logon by an ftp site, it is possible to configure defaultLogonDomain in the authentication settings (such as basicAuthentication)
If the FTP user name is to be embedded in the URL (as per RFC1738)  then the  "\" and "@" signs have to be url escaped with %5C for the “\” and %40 for the “@”. 
In the examples to follow I used color coding to differentiate between the hostname that is part of the user name and the hostname used to specify actul. Brown color highlights the user name stored in the URL.
ftp.contoso.com@ftpuser can be added to URL as   ftp:// ftp.contoso.com%5Cftpuser@ftp.contoso.com/
 joe@ftp.contoso.com can be added to the URL as   ftp://joe%40ftp.contoso.com@ftp.contoso.com/
 