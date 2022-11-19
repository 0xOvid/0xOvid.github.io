---
layout: post
title: "eLearnSecurity Certified Penetration Tester eXtreme (eCPTXv2) Review"
date: 2022-11-19
categories: CATEGORY-1 CATEGORY-2
permalink: /_posts/eCPTXv2_review
---

The following is a review of the eLearnSecurity course ‘Advanced Penetration Testing’ and the exam for the ‘eLearnSecurity Penetration Tester eXtreme’ (eCPTXv2) certification exam.

*TLDR;* To be ready for the exam do Offshore from HTB, and CRTP from PentesterAcademy… in terms of difficulty the exam is equal to something like the machine Anubis (substitute docker with a network) + Sizzle on HTB and you get a general idea.

# Course

This exam and course is all about Active Directory in the enterprise environment and how to bypass EDR tools, this is the most advanced penetration testing course offered by eLearnSecurity/INE and requires you to string together many different technologies to be successful. Overall I liked the contents of the course which introduces you to the following topics:

- **Social engineering and phishing** - gives a brief insight into the context of phishing emails and simple obfuscation of phishing emails using office documents.
- **Red Teaming Active Directory (AD)** - This section of the course is more or less just a huge information dump of everything Active directory.
- **Red Teaming Critical Domain Infrastructure** - How to attack MS SQL, Exchange, and WSUS servers
- **Evasion** - Goes through obfuscation encoding, userland rootkits etc., and aims to prepare you to create ways of bypassing EDR

Overall a lot of useful information is presented in the course and associated labs, however, the course is starting to show its age, the general gist of attacking AD is still highly relevant but most of the other techniques like evasion and phishing are more or less useless after the course. Another point of criticism is that the course materials are more like an information dump than an actual structured examination of how to attack an AD environment, I would recommend that you start off by reading through the different lab solutions and then go in afterward and look at the course materials so that you have some context of how these different attacks are relevant.

The course is best used supplemented by other resources like hack tricks, hack the box, and other learning platforms like pentester academy, and from what I have heard zero point security also does an amazing job at introducing AD attacks.

The labs of the course are decent but the AD labs are outdated and you will struggle to follow along with the solutions as most of the tools used are depreciated or plainly don't work.

However the course still is not without its merits and the solutions for the labs - while not strictly relevant showcases some nice points on the methodology of an attack and how misconfigurations are strung together to get to Domain Admin (DA)

# Exam

The exam is a beast and took me two attempts to get. It is 48 hours and there is enough to do! you are expected to exploit multiple roads to get to DA, each of which takes time to figure out and exploit, this is where experience really comes into play! You need to have your tools ready and know how to use them. To successfully clear the exam I have the following recommendations:

- If in the budget do the Pentester Academy certifications: CRTP, CRTE, and PACES as the material there is very thorough and gives a lot of context missing in the eCPTXv2 course
- Do the HTB Pro Lab Offshore twice, once with windows and once with kali/linux - try running AD attacks using Windows-based tools like Rubeus etc. from the windows machines you compromise and next with tools like impacket etc. on linux. Also, get comfortable with pivoting.
- Also on HTB do the following machines, they are great and really give insight into how to attack active directory (basically all the AD stuff they have!)
    - Forest
    - Sauna
    - Intelligence
    - Sizzle
    - Blackfield

If you do the above as well as take good notes on the different attacks and tools from the course you should be able to pass the exam no worries (maybe not on the first try ;) )

# Final Thoughts:

All in all, I really enjoyed the journey this course put me on, it is a shame that the course leaves something to be desired but prepping and taking the exam was awesome and I learned a ton! … oh yeah and maybe know some .NET *wink*

# Resources:
- [https://h4ms1k.github.io/Red_Team_Active_Directory/#](https://h4ms1k.github.io/Red_Team_Active_Directory/#)
- [https://github.com/0xJs/CRTE-Cheatsheet](https://github.com/0xJs/CRTE-Cheatsheet)
- [https://philkeeble.com/certification/PentesterAcademy-Red-Team-Labs-Review/](https://philkeeble.com/certification/PentesterAcademy-Red-Team-Labs-Review/)
- [https://huskyhacks.dev/2021/03/20/ecptx/#:~:text=eCPTX has incredible course material,take you the free retake](https://huskyhacks.dev/2021/03/20/ecptx/#:~:text=eCPTX%20has%20incredible%20course%20material,take%20you%20the%20free%20retake).
