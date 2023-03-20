---
layout: post
title: "eLearnSecurity Certified Incident Responder (eCIR) Review"
date: 2023-03-07
categories: CATEGORY-1 CATEGORY-2
permalink: /_posts/eCIR_review
---

*TL;DR:* If you are comfortable using a SIEM, writing queries, and know your way around inspection of data like network traffic you should be good to go for the final examination.

# The course
The course is in-depth and gives much detail into the different aspects of intrusion detection via SIEMs and network traffic monitoring. Some of the key areas covered during the course are the use of different SIEM tools and how they can be used to detect the different parts of the MITRE attack chain. The key points here are understanding the different logs (mostly windows) and how they can be used to detect an attacker and track their activities. During the course, you will be introduced to different attack vectors, and TTPs and how these can be detected in different SIEM solutions (ELK and Splunk). An introduction to the general IR process will also be provided with examples of how the different steps tie together and what activities are involved in each.
The different topics are:
- Incident handling process – what is the incident response process and what happens at each phase
- Traffic and flow analysis – How are incidents detected by looking at network traffic using tools like Snort, Suricata, Bro, and Wireshark
- SIEM tools and endpoint analytics – How can SIEM tools like Splunk and ELK be used to detect incidents, what are events and what can they tell us?

# Exam
The exam mirrors a real-world investigation into an incident, where you are tasked to figure out the level of compromise and what has happened, and what are some recommendations for the next steps. A tip for the exam is to be confident with writing custom queries in the different SIEMs covered during the course and to know how to read the different log types covered in the course, as well as have a general idea of what bad looks like.

# Conclusion:
Overall I was very happy with the course and its content, it is a great starting point for someone who wishes to get more familiar with the general work of intrusion detection such as the work done by SOC analysts. The course covered the different aspects of SOC work in good detail, and if you go through it and do the labs one or two times, you should have no issues passing the examination.

# References
- https://dsxte2q2nyjxs.cloudfront.net/Syllabus_IHRPv1.pdf
- https://drive.google.com/file/d/1r8i4xzK5AGaOdF0BWBOXV8t2jbsvwtDy/view
