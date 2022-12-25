--- 
layout: post
title:  "Reusing paralel port cables"
datetime:   2016-10-08 19:32:59
categories: obsolete cables paralel port
disqus: true
bio: false
---
Not so long ago I ordered preassembled ESP8266 based Wifi module, it is of ESP-01 form factor with a male pitch connector that can be readily used with Dupont wires. This board exposes serial communication pins, the minimal 4 control pins, GPIO0, GPIO2, CH_PD and ReSeT and VCC, GND of course. It also has an on-PCB Wifi Antenna etched on the PCB, which is sufficient for shorter range applications. There is an inconvenience with this module though, it is not breadboard friendly, connector on its own cannot straddle the two sides of a standard breadboard.
![ESP8266 based Wifi module]({{ site.url }}/assets/a77600ab967698f35f55b3c0c8db0357/001.jpg){:style="margin:0px auto;display:block"}  
![ESP8266 based Wifi module]({{ site.url }}/assets/a77600ab967698f35f55b3c0c8db0357/002.jpg){:style="margin:0px auto;display:block"}

I am sure many people still remember how printer port with DB25 connector looks, interestingly enough one can buy a new computer motherboard even today, that has paralel port header although the parallel port interface today is virtually non-existent because of the rise of USB devices. DB25 connector is quite outdated now, but I have seen that it is being used in various home made electronics projects.  
  
So what is so special about DB25 connector ? Probably nothing, but its IDC connector on other end of the ribbon cable can be used to interface ESP8266 Wifi module and connect it to breadboard using jumper wires. IDC connector fits perfectly for this purpose and module does not sit too tightly, it can be easily taken out of connector without any risk of bending pitch connector.
![ESP8266 based Wifi module]({{ site.url }}/assets/a77600ab967698f35f55b3c0c8db0357/003.jpg){:style="margin:0px auto;display:block"}  
 I have seen same type of wifi module without this pitch connector, that comes with pin headers instead, that could be used with prototyping breadboard without any issues. They could be just desoldered also, but this time I am not confortable with desoldering them. Also I have used IDE hdd ribbon cables for this purpose as well when playing with 8x8 led matrix.
![ESP8266 based Wifi module]({{ site.url }}/assets/a77600ab967698f35f55b3c0c8db0357/004.jpg){:style="margin:0px auto;display:block"}  

I find it amazing that these obsolete computer parts can be repurposed and used for solderless prototyping. 
