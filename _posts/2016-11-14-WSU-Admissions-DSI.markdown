---
layout: post
title: Scholarship Evaluation Software
date: 2016-11-15 00:00:00 +0300
description:  # Add post description (optional)
img: dsi.jpg # Add image post (optional)
tags: [Projects, Work, News] # add tag
published: true
tags:
  - Projects
  - Work
  - News
layout: post
description: null
img: 'dsi.jpg'
---

## Distinguished Scholar Invitational
Each year, Wichita State Admissions Department holds an day of group evaluations for a series of scholarships. This event hosts hundreds of graduating high school seniors and dozens of honored evaluators. As recently as 2015, all of these evaluations had been done on paper. In 2016, Ennovar Software designed and developed a browser-based web application to streamline the process of capturing and analyzing the evaluations.

## Archetecture
The app was built in two sections, a front end with React.js and a Ruby back end. The two were connected via API, and served on independed virtual machines.

This was a event-based, time-critical tool. It was only going to be used for 10 hours each year. Additionally, the softare was going be run on hardware provided by the end user. Unknown devices, unknown networks, time sensitive and critical data. In order to ensure access, we built multiple caches, storing data locally to prevent loss in the event of connection errors. We wanted the users to not be influenced by the form factor, as well as keep costs low, so we published a mobile-first web application. 

We worked with the Human Factors Lab at Wichita State University to leverage the experience for research purposes. 

## Product
The software required four main components: Populate, Verify, Evlauate, and Report. Each of these components moved and augmented data about the Students and the Evaluators.

### Populate
The Admissions Office worked with IT Services to collect the Student and Evlauator information. Once collected, the data was cleaned and migrated into the App's database. There are two sessions per event, and each session had two sections. Each Student was in different room for each section, and Evaluators stayed in one room for the session.

### Verify
Instead of joining Student and Evaluator accounts, we opted for a simpler solution of a Section Code. The codes were a combination of two six letter words, to be unique but also not completely forign. The Section Codes were physically placed in each room, so each participant could enter the Section Code they saw in their room. With the email address they provided, and we could ensure everyone was in the correct room.

Because our clients wanted the agility to assign and reassign Studens and Evaluators ad hoc, we chose not to connect the Room/Student/Evaluator object. Instead, we built the connection on the fly based on everyone selecting the code, and letting the Evaluators confirm the presence of the Students verbally. A good old "Hi. How are ya?"

Once Studens and Evaluators were situated, we could get down to business.

### Evaluate
Each Evaluator could give each Student an evaluation based on the criteria set by the Admissions office, and then a ranked choice vote.

All we needed to know what the scores. Evaluators provided two kinds, a rank (each Student was stratified from 1 to 10) and a value (each Student was given between 0 and 100 points). The software collected each of those with verification that each step was complete before a "Finish" action. 
 
### Report
After the evlauations, the App could generate a real time report of based on the evaluation scores reported.

### Results
Out of the gate, the research showed that by using technology instead of a pen-and-paper, the university left a better impression with the prospective studens and parents.

However, the software also reduced the generation of results exponentially. In previous years, results would take weeks to tabulate and compute. The client was able to watch scores come in real-time. A reduced the cost of the running event, as well as improving the image with the Students, was a significant win.

The most problematic aspect of the software was the university wifi and poor cellular reception in the various rooms where Evaluators were placed.