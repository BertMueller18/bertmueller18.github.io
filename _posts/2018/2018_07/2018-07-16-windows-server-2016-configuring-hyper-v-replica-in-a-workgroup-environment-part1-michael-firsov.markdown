---
layout: post 
title:  "Windows Server 2016:  Configuring Hyper-V Replica in a workgroup environment – Part1 | Michael Firsov" 
date:   2018-07-16T10:34:18.252Z 
categories: server2016 hyperv hypervreplica certificate pki security
link: https://michaelfirsov.wordpress.com/hyper-v-replica-in-windows-server-2016-configuring-certificate-based-authentication-part1/ 
tags:
  - links
ogtype: article 
---

> Windows Server 2016: Configuring Hyper-V Replica in a workgroup environment – Part1
In contradistinction to workgroup clusters which were made available only in Windows Server 2016 – I wrote about them in Windows Server 2016: Testing Workgroup Cluster – Part1 and Windows Server 2016: Testing Workgroup Cluster – Part2 – certificate based replication was presented in the earlier version of Windows Server: the possibility of having a non-domain replica server is a great feature for any company, not speaking of the ones with only 2-3 servers at their disposal.
In a workgroup environment the most common way to create the certificates for Hyper-V hosts was to use the makecert utility but, given that this utility is depricated now and the new cmdlet New-SelfSignedCertificate  is available instead in Windows Server 2016, the process of configuring workgroup replicas became a bit easier. In these two articles I’d like to walk all the steps required for setting up replication in Windows Server 2016 workgroup as well the steps required for the testing of the newly-created replica.

It is ridiculous but I failed to find any COMPLETE step by step explanation from MS regarding setting up replication in a non-domain environment so I will explain here all issues an administrator may be facing with while configuring replication according to the few articles found on msdn/technet sites.

Let’s get started by finding out whether any prerequisites exist for deploying a workgroup replica.