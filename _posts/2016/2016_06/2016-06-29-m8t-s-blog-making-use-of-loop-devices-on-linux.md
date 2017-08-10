---
layout: post 
published: true 
title: "m8t's blog: Making use of loop devices on Linux" 
date: 2016-06-29T16:24:51.613Z
categories: linux
link: http://blog.m8t.in/2009/05/making-use-of-loop-devices-on-linux.html 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## Making use of loop devices on Linux
This post is about the loop devices on Linux.

The loop devices are a possibility under Linux to mount regular files. It is often used to mount an iso image, but it can also be used to play with Raid, LVM, or a file system.

To use the loop devices it is mandatory to load the loop module: 
```bash
modprobe loop
```
. This will create the loop devices /dev/loop0, /dev/loop1, etc.

Remark: work inside a tmpfs like /dev/shm to gain speed when running tests.

File-System
Creating a file-system out of a file, plus being able to mount it, works as follow:
Create a file of a hundred mega-bytes:

`dd bs=1M count=100 if=/dev/zero of=output`

Format the file:
`mkfs.ext2 output`

Mount the file with a loop device:
```shell
mkdir loop-mount
mount -o loop output loop-mount
```

When using the option ”-o loop” the first available loop device is taken. It is possible to select the loop device to use by giving the option ”-o loop=/dev/loop0”.
To check that the device is perfectly mounted, run ”mount”. It displays a line like that one:
/dev/shm/output on /dev/shm/loop-mount type ext2 (rw,loop=/dev/loop0)
It is possible to create files and directories within loop-mount, then unmount the device and remount it back.

Raid
Using loop devices is very convenient when training with Raid for instance. To create usable devices for a Raid, it works as for a file-system, except that instead of mounting the file as a loop device they must be setup with the tool ”losetup” that is part of the Linux utilities. In fact, it is not possible to prepare devices for a Raid that are already mounted, and losetup makes a loop device in /dev/ ready to be mounted in a way that it is possible to run 
```bash
mount /dev/loop0 mount-point
```
” instead of 
```bash
mount -o loop file mount-point.
```
Preparing a Raid5 works as follow:
Create 3 files:
```shell
dd bs=1M count=100 if=/dev/zero of=0  
dd bs=1M count=100 if=/dev/zero of=1  
dd bs=1M count=100 if=/dev/zero of=2
```

Format the files:
```shell
mkfs.ext2 0
mkfs.ext2 1
mkfs.ext2 2
```

Setup loop devices:
```shell
losetup /dev/loop0 0
losetup /dev/loop1 1
losetup /dev/loop2 2
```

Prepare the Raid5 device:
```bash
mdadm --create --verbose /dev/md0 --level=5 --raid-devices=3 /dev/loop0 /dev/loop1 /dev/loop2
```
Mount the Raid5 device:
```bash
mount /dev/md0 mount-point
```
