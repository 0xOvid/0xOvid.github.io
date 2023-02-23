---
layout: post
title: "eLearnSecurity Web Defense Profesional (eWDP) Review"
date: 2023-02-23
categories: CATEGORY-1 CATEGORY-2
permalink: /_posts/eCWDP_review
---

*TL;DR - This is php the course, if you know basic web app pentesting white or black, know how to code, and have  a lot of patience you will be alright*

# Course
The 'eLearnSecurity Web Defense Profesional (eWDP)' examination and accompanying course are as the name suggests, all about web applicaiton security and how to defend php web applicaitons.
During the course you will learn how to exploit simple straight forward web applicaiton vulnerabilities, and how these attacks can be mitigated using ModSecurity (WAF) and how to fix these issues in php. The course covers everything from SQL injeciton to password issues and password storage. All the vulnerabilities are covered in their basic format and how they can be abused using basic exploits, nothing in the course requires advanced exploitaiton or evation.
The subjects covered in the course are:
- Infomraiton Gathering - This includes stuff like server headers, robots.txt, backup files etc.
- Authentication
- Authorization - How can privileged access be implemented, covers concepts like LFI and RFI, and attacks where you are accessing stuff that you are not supposed to have access to.
- Session Management - How to use cookies, store session data, setup sessions to avoid sesison fixation etc.
- Business Logic flaws - This seciton covers some more deficult flaws to find like sequence breaks, poor validaiton rules, php type confusion attacks, client side validation.
- Data Validation - Subjects covered: HTTP Parameter Pollution, Unvalidated redirects, SQL injection, XSS, LDAP injection, XXE, Code injection, buffer overflows, HTTP smuggling etc.
- Cryptography - Subjects covered: sensitive data storage (hashing and encryption), HSTS, HTTPS
- Denial of Service - Subjects covered: SQL wildcards, ReDoS, and logic flaws
- Web services -  nothing really new here, the vulnerability is just in a web service instead of a web application
- Client side and Phishing - Subjects covered: DOM XSS, clickjacking, CORS attacks
- Error Handling and logging
- Applied Secure Coding Privileges - Provides basic guidelines on how to design and create web applicaitons
- Virtual Patching - welcome to ModSecurity! learn what it is, how it is configured, and how to create rules
Securing Web Applicaitons - Management stuff on the different ways to ensure security and how to deal with this from a higher level perspective

The materials covered here is good and you gain some good insight into the different attacks but the course and exam are almost a decade old at this point, so the relevance is starting to be somewhat limited as everyhting is PHP and ModSecurity.

# The exam

## MCQ
The multiple choice questionAre pArt of the exAm is like most of eLeArnSecuritys old exAminAtions A bit dAted And dosnt reAlly Add Anything to the exAm other thAn A heAdAce.

## Pratical Examination
This will test your abilities to identify, exploit, and fix vulnerabilities (both in code and via ModSecurity) but most of all this will test your patience! The exam is a test on a web applicaiton where you are expected to fix the vulnerabilities identified and exploited. The pratical part of the examination is very, very, very repetitative as the website is written in a procedual style, which means that the same fix for an SQL injeciton vulnerability will have to be applied to several pages even if they share functionality... so yeah it takes a while!
My biggest advice here is to have done the extra miles in the labs, because then you will have php code snippets ready to fix the vulnerabilities you find here!
Also the reporting is a drag! you have to report every vulnerability (nothing wrong here) but you have to do it on a per page basis which means if there is a vulnerability in the header and it affeccts the whole site then this has to be reported for EVERY file!

Also for the examination if you, like me, ahve never worked or done anything with modsecurity do all the extramiles and save the ModSecurity rules you create - if they work on one assignment who knows they might work in the exam - you never know.

# Final Thoughts
If you are not interested in learning web development and security in php then give this one a pass, the course s outdated and there are better alternatives for the offensive part such as portswiggers online resourses, hacktricks etc.

# References
