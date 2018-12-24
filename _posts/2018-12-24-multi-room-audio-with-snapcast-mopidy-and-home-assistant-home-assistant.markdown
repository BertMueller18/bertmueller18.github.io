---
layout: post 
title:  "Multi-room audio with Snapcast, Mopidy, and Home Assistant - Home Assistant" 
date:   2018-12-24T10:18:45.578Z 
categories: homeautomation networking nodered
link: https://www.home-assistant.io/blog/2016/02/18/multi-room-audio-with-snapcast/ 
tags:
  - links
ogtype: article 
---

> Multi-room audio with Snapcast, Mopidy, and Home Assistant
 February 18, 2016  happyleavesaoc  four minutes reading time  How-To Comments
Would you like to listen to music in every room in your home, controlled from one source? Then multi-room audio is for you.

Multi-room audio can be achieved by having a computer attached to speakers in every room. On each computer, services run to play and/or control the audio. With this DIY approach, the kind of computer and speakers is very much up to you. It could be your desktop computer with attached powered speakers, your HTPC hooked up to your TV and receiver, a Raspberry Pi with Amp or DAC, or even an Android device.

You’ll need two key software packages, besides Home Assistant. The first is Mopidy, a music server that can play local files, or connect to streaming music services like Spotify. The second is Snapcast, which enables synchronized audio streaming across your network. Both can be integrated into Home Assistant. Each room audio device will run an instance of the Snapcast client, and optionally a Mopidy instance. Your server will run a special instance of Mopidy and the Snapcast server.

Finally, you also need a player to control Mopidy. Any MPD-compatible player will work, and there are several Mopidy-only web-based options available. On Android, Remotedy is particularly nice since you can access multiple Mopidy instances in one place.

Home Assistant will provide device status, and volume control for each room. If you want to play music in all your rooms (on all your clients), access the server instance of Mopidy. If you want to play music only in a specific room, access that specific Mopidy instance. If you’re using a web UI for Mopidy, you can add links to each instance in Home Assistant with the weblink component.