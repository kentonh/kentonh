---
layout: post
title: Need a code name for your new project?
date: 2019-02-28 00:00:00 +0300
description:  # Add post description (optional)
img: prjctnamr.png # Add image post (optional)
tags: [Projects, Work, Fun] # add tag
published: false
---

##[See the Project](https://kentonh.github.io/ProjectNameGenerator/)

## Code Names for Projects and Initiatives
Most of the time, when I start working on something, it's purely conceptual. There's no marketing or naming conventions nailed down. There's no official title determined. I have found through my own experience that a code name is much more fun than a ticket number or logical title like "New Website" or "Self Hosted Audio Playback System."

## This came up one too many times
In those instances, coming up with something on the fly and out of thin air led to human bias led to very similar project code names; like "Solar Flare" and "Lunar Eclipse." Or "Rattlesnake" and "Mongoose" for another example. Thus, I believed randomness and software could help.

## PRJCT NAMR
I forked [NAMR, for generating JavaScript Framework names](https://digisz.github.io/javascriptframeworknamegenerator/), which worked by pulling a random work from a txt file and appending ".JS" and using an API to define the word.

I used what was built to start the parsing and selection of the word. I also kept the design. I then augmented the process by adding in a second random word, typically an adjective, and parsing the definition json responses to choose a random one from the list for each word. For more fun, I added random microcopy to the button and processing placeholder text.

Google Analytics is being used to track the visitors, initial code name generations, and then each subsequent project name generated.
