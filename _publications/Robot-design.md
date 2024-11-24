---
title: "Multitask Robot Design"
collection: publications
category: manuscripts
permalink: /publication/2010-10-01-paper-title-number-2
excerpt: 'Desinged Multitask robot with Image processing and deeplearning'
date: 2021-03-03
venue: 'University Of Moratuwa'
slidesurl: 'http://academicpages.github.io/files/slides2.pdf'
paperurl: '[http://academicpages.github.io/files/paper2.pdf](https://github.com/GevinduGanganath/Robocop.git)'
citation: 'Your Name, You. (2010). &quot;Paper Title Number 2.&quot; <i>Journal 1</i>. 1(2).'
---


We have designed a multitasking robot with the following root tasks: line following, wall following, object detection, color detection, carrying objects to designated places, and shooting a ball object to a goal position.

This project was implemented in C++. For the line-following task, we used an IR sensor array and implemented a PID algorithm (Proportional, Integral, Derivative), which allowed us to achieve accurate line following.

Wall following was carried out using two ultrasonic sensors, and we also used a PID algorithm for this task, which resulted in precise wall following. Additionally, we needed to track whether we had visited a specific location or not, so we used a cell-filling method to structure the wall maze as a grid. We kept track of visited nodes, and at each junction, we determined the direction (left or right) based on this data.

For object detection, we used a Raspberry Pi camera module. We applied image processing techniques to detect cylindrical and square-shaped objects by checking basic geometric relationships. We extracted geometric features using image processing, including corner detection and edge detection, and calculated distances to determine whether an object was square or cylindrical.

After detecting objects, we needed to locate matching holes in which to place these objects. This task was completed using mechanical arms on the robot, and we reused the above image processing techniques for this purpose.

Next, based on a given color, we needed to pick up a colored ball and exit the color-specific area, follow a new line track, and shoot the ball into the relevant goal. This was accomplished using a mechanical solenoid.

For floor color detection, we used an additional color sensor module. This was necessary because the objects were placed in areas with different floor colors.
