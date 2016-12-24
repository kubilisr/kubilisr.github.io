---
layout: post
title:  "Merry Christmas!"
date:   2016-12-24 16:25:08
categories: oled holidays fun ssd1306xled
disqus: true
---

<iframe width="560" height="315" src="https://www.youtube.com/embed/6gDxQJrkgGE" frameborder="0" allowfullscreen></iframe>
Got some spare time before holidays and I decided to assemble some simple electronic greeting prototype and this is a result of me finding some [free Christmas related icons](http://sivioco.com/blog/free-christmas-vector-icons){:target="_blank"} on internet, I created a thresholded bitmaps of these images <img src="https://static1.squarespace.com/static/5006e72724ac70f8fbc68c5e/t/508024bee4b03711ad4edd2f/1350575295881/christmasicons.jpg?format=750w" alt="christmas icons">  
and converted them to hex arrays using [bitmap converter program](http://en.radzio.dxp.pl/bitmap_converter){:target="_blank"}. In video above you can see 0.96" OLED display hooked up with jumper wires to Attiny85 microcontroller on breadboard, here I am using [ssd1306xled](https://bitbucket.org/tinusaur/ssd1306xled){:target="_blank"} library drivers to display images on screen, ssd1306xled is provided provided by - [The Tinusaur Project](https://tinusaur.org/about/){:target="_blank"}. ssd1306xled library already comes with some test examples which can be easily modified for your needs. Nothing mega epic, but that is just the beginning. 
