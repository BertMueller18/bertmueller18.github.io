---
layout: post 
title:  "Ubuntu ZFS Samba share - superMaru" 
date:   2018-05-26T09:07:29.297Z 
categories: zfs linux ubuntu samba security
link: http://www.supermaru.com/2017/05/ubuntu-zfs-samba-share/ 
tags:
  - links
ogtype: article 
---

> Ubuntu ZFS Samba share
05/16/17 / /	 / linux	/ cli, linux, smb, ubuntu, zfs
In my previous posts regarding setting up ZFS on Ubuntu 16.04, I had referred to Aaron Toponce’s website on doing additional configuration to ZFS such as sharing via NFS or SMB.

In the portion for SMB here: https://pthree.org/2012/12/31/zfs-administration-part-xv-iscsi-nfs-and-samba/, it seems that there is a couple more things to do.

After running zfs set sharesmb=on pool/srv  and zfs share pool/srv, the share will be visible on the network from a Windows computer. However, if you try to access it, you will be prompted by an user authentication prompt. If you try to access as guest, access will be denied.

When running the zfs share command, a file will get created in /var/lib/samba/usershares/[zpool name]

In the file, you will need to look for “guest_ok=n” and change it to: “guest_ok=y”

example:

#VERSION 2
path=/opt/share
comment=Comment: /opt/share
usershare_acl=S-1-1-0:F
guest_ok=y
sharename=tank_export
And finally, to make the directory read/writable: sudo chmod 0777 [path to your ZFS filesystem]