---
layout: post 
published: true 
title: "dd Cheat Sheet – JamesCoyle.net" 
date: 2016-08-04T17:05:24.783Z
categories: linux 
link: https://www.jamescoyle.net/cheat-sheets/1012-dd-cheat-sheet 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## dd Cheat Sheet
Tags : Backupcheat-sheetddI/OLinuxrestore

Category : Cheat Sheets

Get Social!
dd is one of the most versatile IO tools available for Linux. It’s used in a variety of ways ranging from Disk Benchmarking through to creating SWAP files and copying downloaded disk images to physical disks.

dd takes the following common switches:

if is the input file name and location.
of is the name and location of the output file.
bs is the block size that will be used to read and/ or write the file. Increasing this can help with performance  or dictate how much data will be read or written.
count is the number of blocks that will be used.
seek is the number of blocks on the output file that will be skipped before writing any data.
skip is the number of blocks that will be skipped on the input file before starting to read data.
conv is a comma separated list of additional parameters that can be used. See the man dd for more information.
The below headings will list a few example uses of dd in a typical Linux environment.

Backup disk partition with dd
You can use dd to copy an entire disk partition to a virtual disk file. This can be useful for creating a backup or to clone the disk to another machine.

1
dd if=/dev/sda1 of=~/localdisk_sda1.img
You can use this method to read a CD-ROM, USB drive or Flash disk to a file in the same way – just make sure the device is inserted and point the if= part of the dd command to the relevant /dev/ device.

You could also compress the image as part of the process with gzip.

1
dd if=/dev/sda1 | gzip -c > ~/localdisk_sda1.img.gz
Restore disk partition with dd
Similar to the above command, you can use dd to replace a disk’s partition with a virtual disk file.

1
dd if=~/localdisk_sda1.img of=/dev/sda1
If you compressed the image then you can decompress it first all in one go:

1
gunzip -c ~/localdisk_sda1.img.gz | dd of=/dev/sda1
Create a fixed size file with dd
You can create a fixed size file with DD that will be created in the location you specify.

1
dd if=/dev/zero of=/root/test bs=1024 count=1
This will create a file in /root/test of 1024 bytes in size. Increase either bs or count to change the size of the file. The resulting size will be bs * count. You can also use shorhand sizes such as K, M and G with bs, for example bs=1G,

1
dd if=/dev/zero of=upload_test bs=file_size count=1
Create a SWAP file with dd
dd can be used to create a SWAP file that can be used as a SWAP device by your computer. This is often needed with smaller instances on Cloud providers such as AWS.

The starting point is the same as the above command to create a file with the size that you’d like to use for swap. See my other blog post for more info.

Split a file with dd
dd can be used to read just part of a file, given offset and length coordinates. The below example will skip the first 100 bytes of the file and output the proceeding 10 bytes (byte 101 – 111).

1
dd if=filetosplit of=partfile bs=1 count=10 skip=100
You could repeat this process to split a large file into multiple smaller files, to be able to email it for example.

1
2
3
dd if=filetosplit of=partfile1 bs=1 count=100
dd if=filetosplit of=partfile2 bs=1 count=100 skip=100
dd if=filetosplit of=partfile3 bs=1 count=100 skip=200
Merge multiple files with dd
You can merge multiple files into a single file with dd. Following on from the above split example, the below will rejoin the 3 file parts into a single file.

1
2
3
dd if=partfile1 of=joinedfile bs=1 count=100
dd if=partfile2 of=joinedfile bs=1 count=100 seek=100
dd if=partfile3 of=joinedfile bs=1 count=100 seek=200
Convert text to lower case with dd
You can use the conv switch with dd to transform ascii text from upper case to lower case and visa-versa. Using lcase and ucase in the conv switch will instruct dd to convert the text as it’s written.

The below example will convert all characters in the filetoconvert.txt. file to lower case.

1
dd if=filetoconvert.txt of=convertedfile.txt conv=lcase
