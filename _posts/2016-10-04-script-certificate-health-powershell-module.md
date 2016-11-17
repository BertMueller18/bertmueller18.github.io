---
layout: post 
published: true 
title: "Script Certificate Health PowerShell Module" 
date: 2016-10-04T18:59:14.608Z 
categories: certificate powershell pki
link: https://gallery.technet.microsoft.com/scriptcenter/Certificate-Health-b646aeff 
tags:
  - links
ogtype: article 
bodyclass: post 
---

The Certificate Health PowerShell module allows you to evaluate the certificates installed on your local system for expiration and deprecated signature algorithms. Using the included functions you can get certificates from the local certificate stores as well as certificates on the filesystem. In addition to getting the certificate health of these certificates an included function, Get-UnhealthyCertificates is designed to integrate with the Nagios monitoring system to alert administrators of certificates that are expired, expiring, or using outdated signature algorithms (i.e. md5RSA, sha1RSA).

 
