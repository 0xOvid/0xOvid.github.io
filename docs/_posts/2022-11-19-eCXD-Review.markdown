---
layout: post
title: "eLearnSecurity Certified eXploit Developer (eCXD) Review"
date: 2022-11-19
categories: CATEGORY-1 CATEGORY-2
permalink: /_posts/eCXD_review
---

This is another awesome course and exam by the eLearnSecurity team, unlike some of their other offerings this course was up to date and there is not much bad to be said about the course. Both the course and the exam proved a wonderful learning opportunity and an awesome challenge.

*TL;DR* - do ROPemporium, read the tutorials by the corelan team, do some pwn challenges and machines from HTB, do the labs, and you should be ready for the exam.

# Course

As hinted above this is one of the better and more updated of eLearnSecuritys offerings, the course and accompanying labs do a really good job of introducing the concepts of binary exploitation and the different ways to achieve code execution in both Linux and Windows environments as well as how to bypass different defensive measures. The course covers everything from ROP chains to egg hunters and the power of w00t. In brief, the areas covered are:

- Linux exploit development
    - Linux stack smashing - introduction to very basic buffer overflow attacks
    - Linux Exploit Countermeasures and bypasses - NX, ASLR, RELRO bypasses etc. this is where the first concepts of ROP chains are introduced via ret2libc
    - Linux Return Oriented Programming - Hands up this is a ROPpery! get ready to get familiar with ROP and its uses.
    - Linux Shellcoding - basics for writing ASM shellcode
    - Linux Advanced Exploitation - This is where the meat of the Linux part of the course is located, you get several different examples of advanced Linux exploits stringing together different concepts from the earlier sections. The labs are awesome and do a good job of explaining the concepts, but if you need more context or something does not click it is always a good idea to see if you can find an alternative source explaining the same concepts in a different way.
- Windows exploit development
    - Windows Stack Smashing - Same as its Linux namesake, but for windows
    - Windows SEH-based overflows - Introducing how windows error handling can be abused for code execution and its uses - not of caution here, be very diligent of the difference in this type of overflows and regular buffer overflows, it is easy to mix the two together and waste a lot of time (I'm speaking form experience)
    - Windows Egghunting - w00t w00t
    - Unicode Bufferoverflows - for this and the above see the awesome defcon talk by offsec ‘DEFCON 16: BackTrack Foo - From bug to 0day’ the video is awesome supplemental info to the course and gives an exelent illustiration of how this might be used and how it is done.
    - Windows shellcoding - you can guess for yourself what this might be about.
    - Windows Return Oriented Programming - Again all hail the ROP

# Exam

The exam is a series of challenges both windows and Linux where you are tasked with exploiting different files under different circumstances. Without spoiling anything, if you have done the labs one or two times and maybe some challenges on HTB, read the corelan tutorials, and done ROPemporium you should be ready to take on the exam. It is an interesting challenge forcing you to be creative in your problem-solving and googling! For some general hints on binary exploitation I have added some notes and resources below, this is by no means an exhaustive list but it should get you going! Happy hacking!

## Exploit Structure
### Windows Basic

```jsx
overflow/junk + eip(jmp esp) + nop + shellcode
```

### Linux Basic

```jsx
nop + shellcode + padding + return_address
```

### Windows/Linux ROP

```jsx
overflow/junk + rop + shellcode
```

To get shellcode executed different methods are used to either make the stack executable of make system calls with code which is already existing

## Common pitfalls

- Check offsets, and offset calculation
- Check memory addresses
- Check the jump address and core dump
- Check the order of the payload
- Check payload on stack i.e. is what we want on stack there? and is it in the right order
- Check execution flow (try replacing shellcode with “\xcc” and see if we get to the breakpoint)
- For Windows:
    - First, check for simple $eip overwrite
    - If not possible check for SEH overwrite
- ROP notes
    - Check functions of the binary.
    - Check gadget order
    - Check if gadgets exist that do more than one of the desired operations.

# Resources
- [https://ropemporium.com/](https://ropemporium.com/)
- [https://www.corelan.be/](https://www.corelan.be/)
- [https://www.youtube.com/watch?v=gHISpAZiAm0](https://www.youtube.com/watch?v=gHISpAZiAm0)
- [https://blog.stalkr.net/2011/04/pctf-2011-22-hashcalc1.html](https://blog.stalkr.net/2011/04/pctf-2011-22-hashcalc1.html)
