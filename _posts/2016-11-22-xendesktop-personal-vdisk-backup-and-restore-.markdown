---
layout: post
title:  "XenDesktop Personal VDisk Backup and Restore"
date:   2016-11-22T21:31:38.155Z
categories: pvdisk xendesktop citrix xenapp
link: http://support.citrix.com/proddocs/topic/xendesktop-7/cds-manage-personal-vdisks.html
---

## XenDesktop Personal VDisk Backup and Restore

Citrix have an detailed article on Managing Personal Vdisks and backing up and restoring them.
This is detailed in the E-docs here

The following shows the process used by RealServe IT in our labs to test the process.
This process is designed to help move a users Personal Vdisk to another catalog.
This could be used to migrate users to a newer environment or recover from a failure.
Essentialy the scripts attach the users personal Vdisk to another Virtual Machine.

The document says the personal Vdisk can only be moved however to a catalog with a master related to the original catalog the Vdisk started life from. This could limit the flexibilty of this process. &#x2014;[XenDesktop Personal VDisk Backup and Restore | ](https://realserveit.wordpress.com/2014/08/19/xendesktop-personal-vdisk-backup-and-restore/)
