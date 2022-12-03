---
layout: post
title: "eLearnSecurity Certified Digital Forensics Professional (eCDFP) Review"
date: 2022-12-03
categories: CATEGORY-1 CATEGORY-2
permalink: /_posts/eCDFP_review
---

*TLDR; Slow labs, old course materials, know the Zimmerman tools and the SANS Digital Forensics poster (red)*

This course gives a good introduction to old-school digital forensics focusing on disk and registry artefacts, but it does not touch memory forensics. However, despite this, you will learn how to recover data from corrupted hard disks and in-depth analysis of registry artefacts. The fundamentals of the course are solid but the execution lacks behind. This can be attributed to this being some of the oldest course content available from eLearnSecurity. 
In brief, the course is more focused on the criminal investigations and traditional law enforcement side of things, though these skills are often directly applicable to cyber security.

# Course
The course contents cover the following topics:
-	Data acquisition – How is forensic data acquired in a manner satisfying legal and regulatory requirements
-	File and Disk analysis – Goes all the way from an in-depth explanation of data, files, and file structures to an analysis of said files e.g. analysing word documents and pdfs for malicious content. The course then details the inner working of disks and how they are made up and goes into detail on every part of their inner workings from how files are addressed on a disk to the differences between HDDs and SSD. Last but not least file structures are covered in detail focusing on FAT and NTFS covering everything from how the file system is built up and how the whole structure of the file system works to file carving, both manual and automatic, and how filesystems can be recovered when corrupted.
-	Windows forensics – This module covers the Windows OS in depth going through the Windows Artifacts (LNK files, ThumbCache, Volume Shadow Copy, JumpLists, Libraries/dlls, Windows Search history, and the Windows recycling bin), Cach files, Windows Registry, Shellbags, USB forensics, Browser forensics, and Skype forensics
-	Network forensics-  hare pcaps are analysed and the course covers how network traffic can be used to retrieve files and support forensic evidence.
-	Log, Timeline and reporting – Lastly the course details methodology for digital forensics and how timelines provide value for the forensics process, and how to create a sound forensic report. And how to analyse windows logs.

The labs, including the exam environment, were more akin to looking at a slide show and definitely left me underwhelmed – it was frustrating being hampered at every turn with slow labs… here there is definitely room for improvement (note that this might have changed since the acquisition of pentester academy and their lab infrastructure).

# The Exam:
It was disappointing that the exam did not include more of the tools shown in the course like autopsy, I can see why it didn’t since these tools automate a lot of the investigation process and do not require the student to have the same depth of knowledge. The exam also seemed quite dated, and slow, especially slow.
For prepping for the exam go through how to recover a corrupted file system, both MBR and GPT (and be able to do this in a hex editor), and have a solid understanding of everything on the SANS Digital Forensics poster (the red one), linked below. And as always check what other people have said and use these as a reference point to ensure that you haven't missed anything ;) 

# Resources
- https://www.sans.org/posters/windows-forensic-analysis/
- https://medium.com/@saqibshabbir/elearnsecuritys-digital-forensics-course-exam-review-c9a42e48271b
- https://www.thecyberunion.com/blogs/elearnsecurity-digital-forensics-professional-review
