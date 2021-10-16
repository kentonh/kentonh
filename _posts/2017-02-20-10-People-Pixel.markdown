---
title: People Pixel
date: 2017-02-20 21:00:00 Z
tags:
- Projects
- Work
- News
- Product Management
layout: post
description: 
img: peoplepixel.jpg
---

## In March 2014
James Steck is a professor of Aeronautical Engineering at Wichita State University. He had an idea to support the Shocker Men's Basketball team with an app that animate the crowd. The first implementation was a simple HTML file with a timed JavaScript color changer. However at Ennovar, my team and I wanted make a larger leap.

## It's so simple

...or so we thought. We started with research into the best way to detect location information from the user device. GPS signal was too week to penetrate the arena architecture. Next, we tried to use a standard location, but update the device display based on time and the compass direction the user was facing. The device compass was not accurate enough and users like to move too much for this to be effective in a crowd of 15,000.

Finally, we decided to use seat numbers to locate each user in the arena. With openCV and Python, we dissected each frame to create the animation as an image. The result produces a JSON array of color and time duration for an X,Y coordinate on a grid. With a CAD seating arena chart, we were able to translate the Section, Row, and Seat numbers for each user to the corresponding X,Y value in our database, and deliver the "seat pixels" to each device.

## Timing is everything

We expected each device to have near identical time across every network. Our assumption was that we could start the animations on all devices based on a simple time sync, but even among identical devices, system time could vary by as much as 40 seconds.

This meant that we needed to create our own syncing system. We did this by passing a timestamp from the device to our server, coupling it with a second timestamp from our server, then passing the couple back to the device. The device would use an algorythem to determine a time shift from our `fixed point of time truth`, and adjust the starting time of the animation by that number of milliseconds.

## The real world

We were able to test the system at scale in some of the last basketball games of the Shocker's 2016-2017 season. While we had success with our technology, the lighting system was not cooperative.
In November, 2017 we were able to use the app with a new arena lighting system that allowed the arena to go dark. This let the devices show with more clarity.

## Local News

In February, 2017 Wichita news station KWCH covered the early tests and development of the software.

<video controls>
  <source src="/assets/video/PeoplePixel.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>