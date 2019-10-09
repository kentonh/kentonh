---
layout: post
title: Scholarship Evaluation Software
date: 2116-11-15 00:00:00 +0300
description:  # Add post description (optional)
img: http://lorempixel.com/975/730/ # Add image post (optional)
tags: [Projects, Work, News] # add tag
published: false
tags:
  - Projects
  - Work
  - News
layout: post
description: null
img: 'http://lorempixel.com/975/730/'
---

## Distinguished Scholar Invitational
Each year, Wichita State Admissions Department holds an day of group evaluations for a series of scholarships. This event hosts hundreds of graduating high school seniors and dozens of honored evaluators. As recently as 2015, all of these evaluations had been done on paper. In 2016, Ennovar Software designed and developed a web-based application to streamline the process of capturing and analyzing the evaluations.

## Archetecture
The app was built in two sections, a front end with React.js and a Ruby back end. The two were connected via API, and served through two different servers.

This was a event-based, time-critical tool. It was only going to be used for 10 hours per year. In order to ensure access, we built the software with a multiple caches to store data locally to prevent data loss in the event of network or connection errors. We wanted the users to not be influenced by the form factor, as well as keep costs low, so we published a mobile-first web application. 

We worked with the Human Factors Lab at Wichita State University to leverage the experience for research purposes. 

## Product
The software required four main components: Populate, Verify, Evlauate, and Report. Each of these components moved and augmented data about the Students and the Evaluators.

### Populate
The Admissions Office worked with IT Services to collect the Student and Evlauator information. Once collected, the data was cleaned and migrated into the App's database. There are two sessions per event, and each session had two sections. Each Student was in different room for each section, and Evaluators stayed in one room for the session.

### Verify
 Instead of joining Student and Evaluator accounts, we opted for a simpler solution of a Section Code. The codes were a combination of two six letter words, to be unique but also not completely forign. The Section Codes were physically in each room, so each participant could enter the Section Code they saw in their roomand the email address they provided, and we could ensure they were in the correct room.
 
 ### Evaluate
 Each Evaluator could give each Student an evaluation based on the criteria set by the Admissions office, and then a ranked choice vote.
 
 ### Report
 After the evlauations, the App could generate a real time report of based on the judging criteria.
