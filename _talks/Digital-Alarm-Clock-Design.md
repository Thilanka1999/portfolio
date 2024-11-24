---
title: "Digital Alarm Clock Design"
collection: talks
type: "Microcontroller Design, C++"
permalink: /talks/2013-03-01-tutorial-1
date: 2021-01-01
venue: "University of Moratuwa"
---


We have designed a digital alarm clock using an ATmega microcontroller, primarily implementing the work in AVR C++. Our alarm clock allows setting the date and time, configuring up to three different alarms, and selecting different tones for each alarm. These are the primary functions our alarm clock performs.

We used the ATMega644P microcontroller and the DS3231 RTC IC. A display module provides the user interface, along with a keypad and two buttons to perform the tasks mentioned above and to power the alarm on and off. Firmware development was done in C++ using Microchip Studio.

A compact and neat PCB was designed with SMD components using Altium Designer. The PCB was fabricated, hand-soldered, and tested to ensure accurate performance. An attractive and user-friendly enclosure was created in SolidWorks, integrating all supporting components.