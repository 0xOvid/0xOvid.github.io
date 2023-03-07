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
- https://medium.com/@sharonlin/useful-registers-in-assembly-d9a9da22cdd9
- https://www.tutorialspoint.com/assembly_programming/assembly_registers.htm
- https://stackoverflow.com/questions/8629188/asm-interpreter-how-are-local-variables-stored
- https://en.wikibooks.org/wiki/X86_Assembly/X86_Architecture![image](https://user-images.githubusercontent.com/117951172/223400904-8e27822f-fb09-47dd-9d4e-ce45f937fa6e.png)
- http://www.c-jump.com/CIS77/ASM/Instructions/I77_0070_eflags_bits.htm![image](https://user-images.githubusercontent.com/117951172/223400955-5b030419-e91c-427b-9feb-8de8ae974c7f.png)
- https://www.cs.virginia.edu/~evans/cs216/guides/x86.html![image](https://user-images.githubusercontent.com/117951172/223400985-6087322b-d604-4036-bef2-ec8e99727572.png)
- https://www.cs.virginia.edu/~evans/cs216/guides/x86.html![image](https://user-images.githubusercontent.com/117951172/223401009-966d9593-a9b9-4406-b25e-eb1a09963e10.png)
- https://learn.microsoft.com/en-us/windows/win32/api/winnt/ns-winnt-context![image](https://user-images.githubusercontent.com/117951172/223401047-4f639b5b-c284-4344-8eb9-1d179ecb6a10.png)
- https://en.wikibooks.org/wiki/X86_Disassembly/Functions_and_Stack_Frames
- https://en.wikibooks.org/wiki/X86_Disassembly/The_Stack![image](https://user-images.githubusercontent.com/117951172/223401148-2dbfc231-7e92-4af3-9b76-e7c296550a0f.png)
- https://stackoverflow.com/questions/4292447/does-the-ret-instruction-add-4-to-esp-register![image](https://user-images.githubusercontent.com/117951172/223401181-8405861a-08fd-4294-860c-8cd843641118.png)
- https://en.wikibooks.org/wiki/X86_Disassembly/Calling_Conventions![image](https://user-images.githubusercontent.com/117951172/223401223-7fb78811-ea96-44fc-8fc9-d75fa624be37.png)
- https://learn.microsoft.com/en-us/windows/win32/api/winnt/ns-winnt-context![image](https://user-images.githubusercontent.com/117951172/223401251-a5119bbc-a13d-484e-85f4-92ae25ba24ea.png)
- https://unprotect.it/technique/ntglobalflag/![image](https://user-images.githubusercontent.com/117951172/223401285-8508efd3-6d43-4ce8-82f3-f074e633d5eb.png)
- https://blog.kowalczyk.info/articles/pefileformat.html![image](https://user-images.githubusercontent.com/117951172/223401360-ded1c602-9066-418f-9abd-572cd7c9baa9.png)
- http://www.sunshine2k.de/reversing/tuts/tut_rvait.htm![image](https://user-images.githubusercontent.com/117951172/223401427-91d9bba4-918c-4eb7-97dd-7f1ecd4c0c34.png)
- https://www.aldeid.com/wiki/PEB-Process-Environment-Block/BeingDebugged![image](https://user-images.githubusercontent.com/117951172/223401457-2b106ec0-a823-44fb-bcf8-983bd402150e.png)
- http://www.jasinskionline.com/windowsapi/ref/c/createtoolhelp32snapshot.html![image](https://user-images.githubusercontent.com/117951172/223401536-fa362d40-0191-4fae-8964-f06d9a2a5c80.png)
- https://kobzol.github.io/davis/
- https://archive.org/details/lena151
