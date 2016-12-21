---
layout: post 
published: true 
title: "linux - Mounting multiple img files as single loop device - Unix &amp; Linux Stack Exchange" 
date: 2016-06-29T16:23:38.083Z
categories: linux raid
link: https://unix.stackexchange.com/questions/17084/mounting-multiple-img-files-as-single-loop-device 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> # Create the files that will hold your data
dd if=/dev/zero of=part-00 bs=1M count=4k
dd if=/dev/zero of=part-01 bs=1M count=4k

# Create the loop devices
losetup /dev/loop0 part-00
losetup /dev/loop1 part-01

# Create a RAID array
mdadm --create /dev/md0 --level=linear --raid-devices=2 /dev/loop0 /dev/loop1

# Copy the original filesystem
dd if=original-file-00 of=/dev/md0 bs=512
# Look at the records written value
dd if=original-file-01 of=/dev/md0 bs=512 seek=<sum of records written values so far>

# Mount the new filesystem
mount /dev/md0 /mnt
You can't simply create a RAID array from the original files because the RAID disks have a specific header where the number of disks, RAID level, etc is stored. If you do it that part of your original files will be overwritten.

You can use the mdadm --build to create an array without metadata but then you really should make a backup first. Or if read-only mount is enough:

losetup -r /dev/loop0 original-00
losetup -r /dev/loop1 original-11
mdadm --build /dev/md0 --level=linear --raid-devices=2 /dev/loop0 /dev/loop1
mount /dev/md0 /mnt