---
layout: post
published: true
title: "Tom's Blog: Setting up a L2TP/IPsec VPN with SoftEther VPN on a Raspberry Pi"
date: 2016-10-23T09:04:33.433Z
categories: vpn ipsec raspberrypi
link: http://tomearp.blogspot.de/2013/11/setting-up-l2tpipsec-vpn-with-softether.html
tags:
  - links
ogtype: article
bodyclass: post
---

> Tom's Blog
General waffle about anything slightly related to computing or electronics. I'm particularly interested in programming (Python, C, Java, PIC assembly, Motorola assembly, Siemens STL/FBD/S7-GRAPH, Crouzet FBD, Rockwell CCW to name a few), computer networks, remote access, network security, linux, amateur radio and raspberry pi. I also like food, beer, Formula 1 and video games.

Thursday, 21 November 2013
Setting up a L2TP/IPsec VPN with SoftEther VPN on a Raspberry Pi
I thought I would share my experience of setting up a L2TP/IPsec virtual private network using SoftEther VPN on a Raspberry Pi...

I have recently started playing around with SoftEther VPN as an alternative to pptpd or openswan/xl2tpd/ppp for remote access.

Point-to-Point Tunnelling Protocol in combination with MS-CHAPv2 authentication has been declared effectively broken by Microsoft, which is a shame because pptpd is very easy to set up and pretty much any operating system you care to name supports it. If you're using PPTP for any kind of production VPN that hosts anything you consider sensitive I strongly suggest you stop and migrate to something better.

Openswan/xl2tpd/ppp works OK but I find it's a bit of a hassle to set up. So I started looking for alternatives and found SoftEther.

I use Windows as my primary operating system, and the server management tool provided will administer servers on any OS which is a handy feature. It provides a fairly decent GUI for configuring the various options.
We will be focusing on configuring it to operate as L2TP/IPsec as most OSs have a compatible client built in, although it supports all sorts of VPNs (it has its own Ethernet over HTTPS VPN which requires their client software; it also supports OpenVPN, MS-SSTP and other things).

At this point the following assumptions are being made:

You have root access or access to sudo.
You are generally familiar with networking (i.e you're familiar with NAT, DHCP, port forwarding, subnets, firewalls, iptables, routing tables etc.).
You have a computer or virtual machine running Windows that can run the Server Manager (if not you can do everything from the command line, it's just easier to configure it with a GUI).

First of all we need to download the software. SoftEther VPN (Freeware) is selected by default. Then choose SoftEther VPN Server as the Component. Select Linux as the Platform. Select ARM EABI (32bit) as the CPU. You'll get a link to the latest version (at the time of writing: Ver 2.00, Build 9387, rtm)

From a terminal use wget to download the software:


wget http://www.softether-download.com/files/softether/v2.00-9387-rtm-2013.09.16-tree/Linux/SoftEther%20VPN%20Server/32bit%20-%20ARM%20EABI/softether-vpnserver-v2.00-9387-rtm-2013.09.16-linux-arm_eabi-32bit.tar.gz

Decompress it:


tar zxvf softether-vpnserver-v2.00-9387-rtm-2013.09.16-linux-arm_eabi-32bit.tar.gz

Compile it:

cd vpnserver
sudo make

It will ask if you want to read the license agreement, choose 1 for yes. Read it. Choose 1 for yes. Choose 1 for agree.
It should then compile and run some checks. At some point you should see a line like:

All checks passed. It is highly likely that SoftEther VPN Server / Bridge can operate normally on this system.

Re-locate the compiled binaries and update some permissions:

cd ..
sudo mv vpnserver /usr/local
cd /usr/local/vpnserver
sudo chmod 600 *
sudo chmod 700 vpncmd vpnserver

Run a final check:

sudo ./vpncmd

Choose 3. Type check and hit return. Everything should pass. Type exit and hit return.

The next step is to create a startup script so it will automatically start with the RasPi. Mine is here. Using the editor of your choice create /etc/init.d/vpnserver (you'll need root access/sudo to write there) and paste the script into it.

Update the file's permissions and run update-rc.d:

sudo chmod 755 /etc/init.d/vpnserver
sudo update-rc.d vpnserver defaults

Now it will start when your Pi starts. You can either reboot or start it manually:

sudo /etc/init.d/vpnserver start

You can verify it is running:

ls /var/lock

You should see vpnserver listed. Now we will set a password on the VPN server:


sudo /usr/local/vpnserver/vpncmd

Choose 1. Hit return for default settings. Hit return for default settings. At the prompt:


ServerPasswordSet

Type a new password, hit return, type again, hit return. If you intend to make the server manageable from the internet make it a good password. We will change the port the server listens on in a moment. Type exit and hit return to close vpncmd.

Go back to the download page. Choose SoftEther VPN Server Manager for Windows and download the file.

Once installed, run it. Select New Setting
