---
# title: "Submission 3: Cyber Security: An Offensive Mindset"
tags: Cybersecurity, UTS, Summer-Studio, Cyber-Security-An-Offensive-Mindset, Sprint-3
---
___

**(NEED TO DO MON-WED-FRI + EVERYTHING I DO IN BETWEEN)**
REFER TO EXISTING REFLECTIONS

This week is about,,,,

## Monday
In the Monday morning Scrum, I spoke with Riley. I asked him what his greatest discovery was over the past week which he stated was that there are way too many readily available resources for hacking which I acknowledged the threat that brings. He also stated that there is a great overhaed on trying to find the right thing to research and focus on as there are so many different interesting resources out there to learn about and learn from.

Another discovery Riley made over the past week was that systems are seriously too easy to crack into, this is brought on by the lack of developers with security knowledge when developing the software, and for vulnerabilities found, the lack of people patching their vulnerable systems is far too high making it open season for hackers to gain access to confidential information.

Rileys greatest struggle this past week has been his scripting and programming ability, for him, getting a functional code of the internet to do a certain purpose was easy, but to develop &/or reverse engineer &/or modify it to do what he needed was quite hard.

From this Scrum, I discovered that many of the students where also suffering from similar issues, many of whom had also taken introductory programming classes and had seemed to not quite grasp onto the basic fundemental concepts of programming/scripting in any language. Perhaps there is a need to change the mentality of the way these classes are taught from the strict must do what we say criteria, to something that aids the student in their end goal in their particlar language/languages and have them creat a prject in this language creating something they want to, as motivation and success in learning comes from an addictive interest to design.

Another key note from this scrum that i've learned is that.......................................................................................................


## Tuesday



**LINK CTF HERE**
**LINK DOMAIN MIGRATION HERE**

## **Wednesday, 20/02/2018 - GROUP¶**
Present a case study on one or more tool(s), and how these tool(s) can be used to break into complex and vulnerable systems.
Brownie points for linking your research to the guest (TBA) presentation that will be held in the morning (10AM - 12PM).
Make sure to include examples.
Keep it high-level.
**Include a capture of the Planner log we created for this**


Your research is to be submitted individually to your sprint 3 submission. Be sure to include your reflection on your learning whilst linking it back to the SLOs. Do not forget your references, academic resources and artefacts.
In your reflection, make sure that your research is technical and low-level.

Wednesday Industry Professionals Presentation (10am to 12pm) by from Deloitte.
Viren Khatri
Simon Baeg – Analyst on penetration testing
Nathan Jones – Cyber intelligence centre (I spoke to him at the end)

What is penetration testing
•	Thinking like criminals to find vulnerabilities so that they can be patched preventing the real criminals for finding them first.
•	Allowed to bend and break rules depending on the situation
•	Legally exploiting a serial device
•	They are white hat hackers 
•	Like to know how things work, computers/cctv/locks/elevators etc, look behind the curtains to figure out how to manipulate these.
•	

What else do we do
•	Attacks, management & cybersecurity
•	Report submissions, what’s wrong, how it was broken, how to fix and avoid that
•	3 types of systems penetrated, Physical (Locks), Human (Phishing tools), Cyber (access cards etc, internal systems i.e. disgruntled employee)
Cool story by ?:
Locked out of home with wife & parents, wife thought sliding door was open, but it was closed, 10 minutes after the beginning, where able to pick the doors by looking at sliding part and fixed part to understand how it’s fixed, they had just screwed the frame from the outside and were able to slide the door open that way.

ONLY PENTEST WHAT YOU’RE ALLOWED TOO
What types of stuff done by all Red Teamers:
Infrastructure – Internal network
Web Application – Externally & Externally developed
Mobile Application Testing/code review- 
Physical Security & Social engineering – Testing if can get into the perimeter to the company
Red team Operations
Citrix + Kiosk breakouts

Penetration Testing
Command injection, navigate through integration directory to get the passwords’ dir “C:\Program Files\hMailServer\Data
Can utilise this to get revers shell into system with netcad with – e option
Utilise Exploit Database – send mail with calmac-milter <0.91…..
Look for publicly exposed exploits that the company has, if enough time then can come up with an exploit yourself, but primarily first part of the job
Buffer overflows are amazingly fun to know and do

Exploiting database weakness to create Administrator Account
•	Database Connection
•	EXEC xp_cmdshell ‘net users DTAdmin Deloitte01 /add’;

Sent out scary email to phish people
•	Popup when you need to authenticate to proxy server
•	They entered in their Username + passwords
•	Got 44-45/150 personal details 
•	After they entered details and click okay a nice little load bar come up to hide any attention

Kiosks:
•	Break out of applications in kiosk by 
•	Browse to any site that allows you to pop up a file explorer in the browser (upload file etc) (Jaycar is locked down using website ACLs)
•	Meterpreter is awesome to utilise

Can XOR signatures can potentially bypass
Don’t like using Metasploit due to it’s simplicity only on time restricted engagements, from a learning perspective going through the code and how it works (no copy or pasting due to trolls with rm/rf commands to delete pc)
Always look at the exploit you’re going to run as there are dangerous commands and scripts in files
i.e. you’re an idiot/remove OS

Famous technique, easy to detect though
•	Break out security system by:
•	Use browser to navigate to file explorer to open cmd
•	Run an .exe in full path it will try open it up as correct 
•	Open up local privilege escalation exploit
•	Run mimicats to download all clear text credentials from memory
•	Running netsc in cmd then login as administrator
•	This will now log into the citrix system so it will now go to citrix admin system

Red Team Operations
•	Name arised from military context
•	Highly skilled penetration testers working towards a set predefined goal
•	Different missions involved include either Physical access, System Access, Social engineering etc or a mix of all
•	Simulates how a real world attacker will gain access to the system
•	Need to do a virtual map of all aspects, rooms/security features+location/weapons used/external features/internal features/patterns/look like you beong there/act confident & go in, utilise a rubber ducky to do a reverse shell exploit within building ALWAYS BE PREPARED TO BE QUESTIONED

Traditional
•	Specific
•	Limited Scope
•	Narrow>

Realistic approach to security testing
•	Realistic
•	Relevant
•	Readiness

Tools used:
•	RFID scanner/duplicator (check what type of card do they use?)(put in iPad sized case/brush past AC/utilise crowded places for effective bumping)
•	Lock picks (3 pin lock used on some old ATMs within 3 seconds)
•	PwnPlug (power + corp ethernet – utilised as an extender to do port forwarding allowing SSH tunnel and what you control, from home office can connect into their network GLAR150 + 4g dongle +optional openboards OS)
•	PowerPwn variant
•	Wifi-Pinapple (Creat fkae hotspots replicating corporate networks)
•	Rubber Ducky (simulates a keyboard), Feed scripts into micro sd card, plug it in and will do everything you want to do quickly (Run  \\etc)
•	Physical hardware testing (i.e. router had pins just had to figure out the different pins and connect via usb-pin adaptor to laptop, UART)
•	Kali/Metasploit/Powershell Empire/


DELOITTE
GRADUATE PROGRAM
VACATIONAL PROGRAM

Cyberfamily/team
Cyber Intelligence Centre (Incident response, pen testing, red teaming, breaking stuff)
Started of in monitoring nd proceeded onto Pentesting
Reach out to them for contact details
Your future.deloitte.au
First year get to work with everything (multiple divisions)
Certifications are paid for in there
Go straight into Analyst work + training in consulting (soft skills) + tech skills

Question work week hours + employment types:
Offer full time and part time grad programs per week 


Dharma decryption tool

Red-teaming
Bro
Don’t expect us to be pros – learnings everything

Artifact: got all three of their email addresses.

ADD WHAT QUESTIONS I ASKED

(TITLE SLIDE)
Good afternoon,
My name is Mitchell and today myself, Max & Harry are going to talk to you about the infamous password cracker, “John the Ripper”.
(NEXT SLIDE)
What is John the Ripper?
(CLICK)
That is an excellent question!
(NEXT SLIDE)



**My presentation role excerpt**
If you’re thinking infamous serial killer Jack the Ripper, (CLICK) you’d be wrong, though they do hold two things in common, their notoriousness and their ability to kill… passwords in our case.
(NEXT SLIDE)
John the Ripper is a password cracking tool that has been cracking around as a prototype since 1995 and officially released for DOS in 1996. Since its introduction, it has cracked billions of passwords at lightning fast speeds and been taken over and continuously improved by Openwall.
(NEXT SLIDE)

For enthusiasts, there is also a community Jumbo version hosted on GitHub for people to commit too, but this isn’t as high quality or bug proof as the free & pro versions developed by Openwall. (NEXT SLIDE)
At current, it supports 15 different platforms including Windows and many distros of unix, there is no bias here (CLICK), it’s one of the most popular password testing and breaking tools as it combines multiple password crackers into a single package including a fully customisable version, while also providing features such as autodetection of password hash types.
(NEXT SLIDE)

As mentioned in the previous slide, out of the box, it can autodetect & run numerous types of plaintext & encrypted/hashed (CLICK) password formats such as:
-Unix crypt(3) hash types: 
-Traditional DES-based
-Bigcrypt 
-BSDI extended DES-based
-FreeBSD MD5-based (used in Linux & Cisco IOS)
-OpenBSD Blowfish-based (used in recent versions of Linux distros and Solaris)
-Kerberos/AFS
-Windows LM (DES-based) hashes and
-DES-based tripcodes


Jack the Ripper uses three types of password attacks, these are:
•	Dictionary Attacks
•	Brute Force Attacks
•	And my favourite - Rainbow Tables
Which I picture look a bit like this.. (CLICK)
But I’ll let Harry go into further details about these.

## Thursday

Thursday I worked 9am-5:30pm



## **Friday, 22/02/2018 - INDIVIDUAL¶**
**((real world test, what I’ve tried, what has failed, Real world test is all that needs to be done otherwise the later needs both done. Include Artifacts.
Do not provide Personally Identifiable Information on personal website.
))**
OPTION 1: Own a vulnerable machine of your choice

VulnHub (see resources below)
HTB - Retired
Cyber Security Challenge Australia - in-a-box
TryHackMe (one of the boxes)
Any other boot 2 root images you find (please reach out if you are unsure)
AND / OR

OPTION 2: Register to the real-world test program

Reminder: the journey is always greater than the destination
Students are expected to be able to explain:
Why they did what they did
Tools they used
Methodologies

Did OWASP Zed Attack Proxy (ZAP)
Issue:
A cookie has been set without the HttpOnly flag, which means that the cookie can be accessed by JavaScript. If a malicious script can be run on this page then the cookie will be accessible and can be transmitted to another site. If this is a session cookie then session hijacking may be possible.
Solution:
Ensure that the HttpOnly flag is set for all cookies.

Issue:
A cookie has been set without the secure flag, which means that the cookie can be accessed via unencrypted connections.
Solution:
Whenever a cookie contains sensitive information or is a session token, then it should always be passed using an encrypted channel. Ensure that the secure flag is set for cookies containing such sensitive information.

Issue:
The page includes one or more script files from a third-party domain.
Solution:
Ensure JavaScript source files are loaded from only trusted sources, and the sources can't be controlled by end users of the application.
Issue:
The cache-control and pragma HTTP header have not been set properly or are missing allowing the browser and proxies to cache content.
Solution:
Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.
Issue:
Web Browser XSS Protection is not enabled, or is disabled by the configuration of the 'X-XSS-Protection' HTTP response header on the web server
Solution:
Ensure that the web browser's XSS filter is enabled, by setting the X-XSS-Protection HTTP response header to '1'.

Issue:
The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.
Solution:
Ensure that the application/web server sets the Content-Type header appropriately, and that it sets the X-Content-Type-Options header to 'nosniff' for all web pages.
If possible, ensure that the end user uses a standards-compliant and modern web browser that does not perform MIME-sniffing at all, or that can be directed by the web application/web server to not perform MIME-sniffing.


## Saturday

I worked 9am-5:30pm

## **Sunday, 24/02/2018 - INDIVIDUAL¶**

I worked 9am-5:30pm

This submission should be a full-fledged reflection of this week (18/02 - 22/02):
Reflect on your learnings from Monday to Friday, be sure to be inclusive of the face-to-face hours and the work you have conducted outside of these hours.
Write about your free-4-all reflection(s) and what you have learnt from each other throughout the week.
Artefacts need to be shown, such as, but not limited to, screenshots, resources, academic references, videos, selfies in class and presentations slides.
If you don’t know already (which you should), click here to see how to submit your weekly submission.













---
Please feel free to [contact me via email](mailto:mitchell.l.tuck@student.uts.edu.au) if you have any questions.




# Reflection


# Useful resources
Link websites/vms/contents etc here



<!--more-->

---
