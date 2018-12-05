---
layout: post 
title:  "ESP8266 Led Strip MQTT Control Lights WS2812" 
date:   2018-12-05T19:16:45.887Z 
categories: iot esp8266 esp32 mqtt
link: https://www.instructables.com/id/ESP8266-Led-Strip-MQTT-Control-Lights-WS2812/ 
tags:
  - links
ogtype: article 
---

> ESP8266 Led Strip MQTT Control Lights WS2812
By billm950 in TechnologyArduino20.936356
DownloadFavorite
 
By billm950Follow
More by the author:

I always wanted under bed led lights so that I can control the mood or even on the family room underneath the tv to get very subtle lighting. I could write rules in OpenHAB and it takes care of the rest. This is a rather simple setup to get everything accomplished over MQTT thanks to the power of Homie Framework with only a few lines of code.

Things to consider before getting started. Depending on the size of your LED Strip of WS2812s, you will need to adjust.

Each LED light consumes about 60 mA, so if you are powering 60, the minimum Amperage would be as follows. As you add more lights, the power requirements also increase.