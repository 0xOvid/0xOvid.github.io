---
layout: post
title: "eLearnSecurity Certified Professional Penetration Tester (eCPPTv2) Review"
date: 2022-12-08
categories: CATEGORY-1 CATEGORY-2
permalink: /_posts/eCPPTv2_review
---

*TL;DR - Do the 5-10 machines on HTB and the Dante Pro Lab, know some pivoting, and you will be good to go*

# Course
This course is the first major step into penetration testing and is an ideal follow-up to the eJPT course. When you first look at the sheer number of different modules and the materials it is very easy to get overwhelmed, I know I did! There is a staggering number of techniques, attacks and exploits to wrap your head around and if this is your first encounter with penetration testing (like it was for me) it is easy to be stun locked. 

So how do you handle all of this information? Well you break it down into smaller pieces, and (pro tip) you realize that most of this stuff is nice to know, but how do you know that? Well if you do some quick googling on penetration testing and CTFs like hack the box you quickly realize that most of the time you are only dealing with a few protocols and attack vectors: SMB, HTTP(S) etc. That being said I highly recommend that you still go through the different modules to get an idea of how different attacks function, but rather than gaining a 100% understanding of each, most of the modules should serve as a reference. Let me give you an example using the network scanner nmap:

Sure it is great if you know a million different ways of scanning stuff and can do zombie scans etc. but give some HTB writeups a look and you quickly come to find that the most used nmap command looks something like this:

´´´
nmap -sC -sV -p- $ip 
´´´

Why is that? that is because the most relevant information will be the open TCP ports and the version of the software running there, the script (-sC) part is nice because it gives a birdseye view of what you might be able to do, i.e. list shares etc.

So how do you get started? I recommend that you go watch an Ippsec or XCT video and then give most of the course materials a quick glance and figure out what is more or less covered, then what some more videos and get started on the slides, videos, and labs!

You will also need to know how to do some pivoting but ill cover that in the exam section!

As for the modules they have the following general contents

- System Security - Introduction to buffer overflows and binary exploitation
- Network Security - External recon, scanning (nmap), enumeration (more scanning), Sniffing/MitM, Exploitation, Post exploitation etc. As the number of different subjects might convey this is where you get a chance to go through most of the different phases of an engagement.
- PowerShell for Pentesters - This might not be totally relevant for the exam but in real life knowing PowerShell is a great skill to have!
- Linux Exploitation - this will teach you Linux and how to hack it! (if anything here does not make sense, head over to HackTricks and it is likely that they have something similar with another point of view)
- Web App Security - General intro to web app testing and exploitation (if you are considering the eWPT, this module covers much of the same info, but the eWPT has a wider variety of info)
- Wi-Fi Security - I did not do this one, but I kind of wish I did (not for the exam but in real life)!
- Metasploit & Ruby - Programming and exploit dev. in ruby (i like python better) and how to write custom modules for Metasploit!

# The exam
Now it's the time! you have studied, and done some HTB machines and feel like you are ready! So some general (no spoiler) info on the exam, you are tasked with doing a penetration test against a small enterprise environment, starting from the outside, so be ready to pivot! You have plenty of time to relax, remember to sleep, go for a walk etc. ... and remember it is not the OSEP or eCPTX so don't over complicate what you are doing! You are not going to be doing over ROP-based buffer overflows and bypassing EDR with userland hooks!

## Additional advice for the exam:
- Take good notes and document as you go! Sure you can come back later and take some screenshots, but why add an additional stress factor? it also increases the likelihood of you forgetting something, so just be an adult and take notes as you go! This is how I like to structure my notes:
  - Subnet#1
    - IP - Machine#1 name
      - Ports/findings
    - IP - Machine#2 name
      - Ports/findings
  - Subnet#2 ....
- Taking pointers directly from the one the only IppSec himself: The tests you do, with for example different payloads, are going to be boolean. You will either get a true or a false result - either you get a shell back or you don't. So therefore when your payload does not work consider doing something altogether more simple, and ask simple questions because you get simple answers. A quick and dirty debugging/troubleshooting model might look like this:
  - Do I have code executing
  - Is there something blocking me
  - What might be blocking me
  - How might I circumvent this
It might be worthwhile thinking of exploitation as an equation where you have different variables like: payload, ports, protocol, and functionality. So write these down and debug each one separately so you get an understanding of why you are failing
- As for the 'how am I supposed top know this?' part of pentesting the following resources are your best friends:
  - HackTricks - Great source of information and references to more or less anything you could want - this will become your best friend! https://book.hacktricks.xyz/
  - Google
  - Superb guide on pivoting (I like chisel!) https://ap3x.github.io/posts/pivoting-with-chisel/
  - Other people's reviews!

So that conclusion, good stuff from eLearnSecurity but take care to not get overwhelmed and stuck in the mire of details of this course, read some write-ups of medium and easy HTB boxes and get come experience on HTB, tryHackMe etc. and you will be certified in no time!
