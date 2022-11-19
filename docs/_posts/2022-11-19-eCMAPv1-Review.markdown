---
layout: post
title: "eLearnSecurity Certified Malware Analysis Professional (eCMAPv1) Review"
date: 2022-11-19
categories: CATEGORY-1 CATEGORY-2
permalink: /_posts/eCMAPv1_review
---

This was and is one of my favorite courses and exams from eLearnSecurity/INE, it has everything: good course material, awesome labs, and an exam that matches. Below is my review of the course, the exam, and some tips and resources to get yourself prepared!

*TLDR;* do eCXD and then be able to read and understand basic assembly, know how to figure out Windows API calls in C, know PE file structures, and general common IOCs and you should be good to go.

# Course

The ‘Malware Analysis Professional’ course by eLearnSecurity is one of the best courses they offer, it is both thorough and gives great detail into malware analysis, and it gives you an idea of how assembly works and how to read it. And the labs associated are just awesome, they are by far the best part of the course! They really show the methodology that you need and what is important to look for when analyzing malware, giving awesome examples of real-world malware and how they are examined, examples include Locky, Killemall, and WannaCry. Here is a short walkthrough of the different sections and in brief what is covered

- **Introduction to Malware analysis** - general stuff surrounding the incident response process and where malware analysis fits in, if you are going to skip anything skip this one
- **Static analysis techniques** - here you are given an introduction to PE file structures and what they can tell you about malware
- **Assembly Crash Course** - as the name suggest you will be learning assembly
- **Behavior analysis** - run the malware and see what happens
- **Debugging and Disassembly** - How to use IDA Pro to look behind the scenes and figure out what the malware can do i.e. source code analysis without the source code
- **Obfuscation Techniques** - Using API monitor and x64dbg to run through the malware and have it deobfuscate itself to show you what is going on

As for how to approach the course, this is an advanced level course and at the start, it felt like everything was going over my head. So instead of getting bogged down in the early labs and not feeling like I was getting anywhere, I went through and read all of the solutions to the different labs and did all of the course work to try to get a methodology together and this turned out to be an awesome approach for this course. As stated previously the solutions and walkthrough for the last sections ‘Behaviour Analysis’, ‘Debugging and Disassembly Techniques’, and ‘Obfuscation Techniques’ really do an amazing job of showcasing the methodology to apply to malware analysis. What I did here was I went through the different solutions from the different labs and tried to figure out the general sequence of things done and why they did them and what they added to the understanding of the malware.

# The Exam

So here is the part that everyone has been waiting for, I won't give you any spoilers but I will give you an idea of what to expect. The exam is more or less the same as the last couple of labs in complexity however there is more stuff to look at and get dug into! If you are comfortable using IDA Pro and x64dbg together with understanding basic PE analysis and having an idea of what malware might be used for you will be just fine. Remember that malware is not supposed to do everything but often has a specific purpose and that if something seems odd it might hide something from you. Some general pointers to ensure success:

- Know how to read API calls in assembly
- Have a general methodology ready for each of the phases: basic static analysis, basic dynamic analysis, advanced static analysis, and advanced dynamic analysis
- Remember what you are trying to do: figure out how the malware works and how to detect it
- Take good notes and have a report template ready to go
- Take breaks, have a coffee, relax stressing won't do you any good
- and have fun, the exam for this one is awesome and the curve ball thrown at you is a fun challenge

Furthermore, I would recommend that you have some experience with dealing with assembly and low-level programming before getting started (not much but some). For me, the eLearnSecurity Certified Exploit Developer (eCXD) was an awesome addition and was a fun way of learning assembly. Also, stuff like HTB and articles online are a huge help to get an understanding of what to expect and how to prepare I have linked some resources below that might help you. If you need some additional practice try using Metasploit to create some payloads for you to get your hands dirty.

# Resources
- Practical Malware Analysis - [https://nostarch.com/malware](https://nostarch.com/malware)
- [https://www.sans.org/posters/malware-analysis-tips-tricks-poster/](https://www.sans.org/posters/malware-analysis-tips-tricks-poster/)
- [https://malgamy.github.io/categories/#malware-analysis](https://malgamy.github.io/categories/#malware-analysis)
- [https://www.varonis.com/blog/yara-rules](https://www.varonis.com/blog/yara-rules)
- [https://github.com/Yara-Rules/rules](https://github.com/Yara-Rules/rules)
