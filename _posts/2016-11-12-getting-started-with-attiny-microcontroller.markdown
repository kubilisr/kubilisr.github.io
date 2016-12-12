--- 
layout: post
title:  "Getting started with Attiny microcontroller"
datetime:   2016-12-11 14:32:59
categories: attny85 avr microcontroller linux
disqus: true
bio: false
---
One day I stumbled upon [Attiny85 Breakout Keychain Game](http://webboggles.com/attiny85-breakout-keychain-game/){:target=”_blank”}, I immediately browsed through parts list to find out what it was comprised of. What brougth my attention is the fact that this keychain game was based on Attiny85 microcontroller. It is the one being suggested in case if you want to [shrinkify your arduino projects](https://www.youtube.com/watch?v=30rPt802n1k){:target="_blank"} i.e. make simple Arduino based projects where you don't need all capabilities of Arduino platform which is based on [ATmega328P](http://www.atmel.com/devices/ATMEGA328P.aspx){:target="_blank"} microcontroller. In case if you are not familiar - Arduino is an open-source electronics platform based on easy-to-use hardware and software. You can read more about it here - [What is Arduino?](https://www.arduino.cc/en/Guide/Introduction){:target="_blank"} 
  
The Attiny85 is small and limited, those who have worked before with it probably have encountered a fundamental problem of not having enough I/O pins, but it is still amazing what you can do with it where the limit is your imagination.  

At once I got captivated by idea making my own keychain game and decided to go with [Tiny AVR Programmer](https://www.sparkfun.com/products/11801){:target="_blank"} from SparkFun, at that moment it seemed acceptable choice and I ordered batch of Attiny85s, that arrived in this anti-static tube inside antistatic bag. Even before ordering anything I checked [Tiny AVR Programmer Hookup Guide](https://learn.sparkfun.com/tutorials/tiny-avr-programmer-hookup-guide/all){:target="_blank"} how to work with this device.

[Blink Without Delay](https://www.arduino.cc/en/Tutorial/BlinkWithoutDelay){:target="_blank"}
