---
layout: post 
published: true 
title: "Relay Module KY -19 (Songle SRD-05VDC-SL-C) - Not Enough TECH" 
date: 2016-11-03T07:42:44.447Z 
link: http://www.notenoughtech.com/raspberry-pi/relay-module-ky19/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

Relay Module KY -19 (Songle SRD-05VDC-SL-C)
OCTOBER 21, 2016 MATLEAVE A COMMENT	781 VIEWS
Tech details:
Control signal: 5V-12V
Current requirements: ~85 mA
Max current: 10A/250V AC or 10A/28V DC
Response time: 10msec
Operating Temp: -25/+70 C

Connectivity:
3 pin connector, pins as follows:

GND: 0V Ground
VCC: 5V-12V
Signal: 5V (see below)
Relay Module KY-19  requires 5V signal to control it. This means that additional circuit is needed to control it through the Raspberry pi GPIO. It is possible to use a transistor to do this. It is possible to control the relay from 3.3V pin, however, depending on the relay module the switch signal may not register. This is mostly an issue due to the current draw. GPIO pins might not be able to provide enough current to the relay. This is especially the case when multiple relays are used.

What does it do?
Relay Module KY-19 is a digital relay module which allows high voltage/current to be switched on or off using circuit-level power. If you wish to control an electric circuit a relay can be used to imitate the mechanism of a manual switch. When a voltage is applied to the module, it allows the flow of the current. This way you can turn on and off various high power devices like lights, motors, appliances.