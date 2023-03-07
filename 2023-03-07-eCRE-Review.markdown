---
layout: post
title: "eLearnSecurity Certified Reverse Engineer (eCRE) Review"
date: 2023-03-07
categories: CATEGORY-1 CATEGORY-2
permalink: /_posts/eCRE_review
---

*TL;DR:* If you have a good understanding of ASM and know how to identify and circumvent common RE techniques you should be good for the exam

#The course
The courseware focuses heavily on the understanding of x86 assembly and goes into a good amount of depth in explaining the different concepts that go into reading and writing assembly. However, as this is quite a complex topic that requires a fair bit of prerequisite knowledge I would highly recommend that this course and exam be done in conjunction with the course material for something like eCXD and eCMAP. The eCRE course teaches its material very well and {{author}} did an amazing job breaking down the core concepts. As with more or less, all eLS courses everything you need to pass the exam is taught in the course

Differences between this course and the eCMAP course, the two look quite similar from a top-level as both involve reverse engineering and understanding of the software. I started with eCMAP and then moved on to eCRE and the main differences are:
- eCRE is a course about understanding ASM and how to identify and read ASM code and functionality. You won't be dealing too much with concepts like Windows APIs etc. the focus is more on how ASM can be used to make a reverse engineer's life difficult and how analysis can be hampered
- eCMAP, you still need to know some ASM to be successful here, but it is more geared towards general ASM code flow analysis with a bigger emphasis on understanding Win API calls and the interaction between OS and code.
In general, eCMAP is a more complete course whereas eCRE teaches a very specific topic.

#Exam
As with many of the older eLS exams, the exam is split into two different parts: an initial multiple-choice questionnaire and a practical evaluation. Though the multiple-choice questionnaire might seem annoying at first hand it makes a lot more sense when thinking of it in context with the practical examination.

- MCQ - this is your standard affair, you get 45 questions and you have to get 40ish right in 90 minutes - preparation is key here! I failed the first couple of attempts at this part because of a lack of preparation, therefore here are some hints for the best outcome: i) have a way to execute and evaluate ASM instructions on hand, I used the following online program {{asm app}}, ii) Be confident with the course material and be sure that you can use it as a reference quickly and effectively I only had access to the online slides show version which meant that searching for key words was not a possibility, so have a screenshot ready of the table of contents ready for each so you won't waste time here, iii) The different parts of the exam can take ant separate times so keep this in mind when scheduling your time, also be sure that you have a good understanding of how PE headers are laid out, what their purposes are and how offsets etc. are calculated.
- Practical part - You made it this far congratulations! now it is time for the fun part! in this section, you are given a binary and 24 hours to analyze it and produce a report (24 hrs for both, not the usual separate timeframes for exam and report). I would recommend that before starting this part you have everything lined up and ready to go! I used the following setup:
	- VM running Windows 7
	- x96dbg
	- DetectItEasy (DiE)
The key concepts here are the same in the course: understand how the code works in general, break it into manageable sections, understand what it tries to do, and only look into what is relevant for your main purpose - i.e. you don't need to read and understand every instruction!. Because of the limited time, I would recommend that you have a generic Word template ready to go for the report. And don't worry if you have done the exercises in the course and in general understood the material 24 hrs should be more than enough to get you through!

#Final conclusion:
Awesome course, the MCQ was a bit frustrating but overall I was happy with every part and thought the execution was on point, I still think this is best taken together with the course (and exam) for eCMAP.

##Reccomended learning path:
If you are looking for recommendations on how best to approach this course using your INE access and possibly can afford some certs. this is how I would recommend approaching the exam:
eCXD -> eCMAP -> eCRE

#References
