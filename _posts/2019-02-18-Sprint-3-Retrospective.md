---
# title: "Submission 3: Cyber Security: An Offensive Mindset"
tags: Cybersecurity, UTS, Summer-Studio, Cyber-Security-An-Offensive-Mindset, Sprint-3
---


# SPRINT 3 - Breaking the Machine

This week will be a journey dedicated to going from Boot to Root, in other words, breaking into vulnerable machines.

## Monday
During Monday morning Scrum, I spoke with Riley. I asked him what his greatest discovery was over the past week, which he stated was that there are way too many readily available resources for hacking which I acknowledged the threat that brings. He also stated that there is a great overhead on trying to find the right thing to research and focus on as there are so many different interesting topics out there to learn about and resources to learn from.

Another discovery Riley made over the past week was that systems are seriously too easy to crack into, this is brought on by the lack of developers with security knowledge when developing the software, and for vulnerabilities found, the lack of people patching their vulnerable systems is far too high making it open season for hackers to gain access to confidential information.

Rileys greatest struggle this past week has been his scripting and programming ability, for him, getting a functional code of the internet to do a certain purpose was possible, but to develop &/or reverse engineer &/or modify it to do what he needed was quite hard.

From this Scrum, I have discovered that many of the students also thought in a similar way as Riley, the excess content on each topic can be overly excessive, and sometimes poorly written. It was also noted that videos should be avoided as they tend to waste a lot of time especially when time is of the essence, it should only be used if a visual walk through is required.

Another key note i've taken away from this scrum is many students had taken introductory programming classes like Riley and had seemed to not quite grasp onto the basic fundemental concepts of programming/scripting in any language. 

Was invited to join another group for Wednesdays Presentation so took them up on the offer. We decided to present about the tool "John The Ripper". We set a basic structure of what content we'd like to present and who was assigned which part. I was assigned Introduction, Harry Technical Details and Max to do a demonstration of it cracking passwords.

## Tuesday
  - Created a plan with my group on what was required to be done in preporation for Wednesdays presentation.
  - Developed content for Wednesdays presentation.
  - Started preparing my website for a Domain Migration from GitHub pages to root9b.tech, routing through Cloudflare for some additional functionality and security.


## **Wednesday, 20/02/2018 - GROUP**
  - Presentation by Deloitte
  - Presented a case study on John the Ripper, and how this tool could be used to penetrate complex systems.
  - Finalising settings and understanding before Domain Migration begins.

# **Industry Professionals Presentation** (10am to 12pm) by Deloitte.
Presenters:
**Viren Khatri** - Manager;
**Simon Baeg** – Analyst/Pentesting;
**Nathan Jones** – Cyber intelligence centre Analyst.

**What is penetration testing**
  - Thinking like criminals to find vulnerabilities so that they can be patched preventing the real criminals from finding them first.
  - Ability to bend and break rules depending on the situation
  - Legally exploiting a serial device
  - Classified as white hat hackers can be divided into three teams, Red - Offensice, Blue - Defensive and Purple - Intimidary ensuring flow of information between the two.
  - Pentesters like to know how things work, computers/cctv/locks/elevators etc, look behind the curtains to figure out how to manipulate these.

**What else they do**
  - Attack, management & cybersecurity
  - Report submissions, for example what’s wrong, how it was broken, how to fix and avoid that in the future
  - 3 key types of systems that are targeted, these are Physical (Locks), Human (Phishing tools), Cyber (access cards etc, internal systems, defence against disgruntled employees)

**Cool story by Viren:**
He was locked out of home with his wife and parents, wife thought sliding door was open, but it was closed, 10 minutes after the beginning Viren was able gain access to their house by looking at the sliding doors, particularly the frame to understand how it’s fixed, the installers had just screwed the frame from the outside, after unscrewing these, Viren was able to slide the door open and gain access to his premises.

**ONLY PENTEST WHAT YOU’RE ALLOWED TOO**
What their Red Teamers do:
  - **Infrastructure** – Internal network
  - **Web Application** – Internally and Externally developed
  - **Mobile Application** - Testing and code review 
  - **Physical Security and Social engineering** – Testing if they can get into the perimeter to the company (in methods similar to Virens story above)
  - **Red team Operations**
  - **Citrix and Kiosk breakouts** - escaping locked down machines such as those used by shopping centre checkouts and interactive map directories

**Penetration Testing**
 Key notes taken:
  - Command injection, navigate through integration directory to get the passwords’ dir “C:\Program Files\hMailServer\Data
  - Can utilise this to get reverse shell into system with netcad with – e option
  - Utilise Exploit Database – send mail with calmac-milter
  - Look for publicly exposed exploits that the company has, if given enough time then can come up with an exploit yourself, but primarily will be do exisiting exploits
  - Buffer overflows are amazingly fun to know and utilise

**Exploiting database weakness to create Administrator Account**
  - Database Connection
  - EC xp_cmdshell ‘net users DTAdmin Deloitte01 /add’;

**Past example task - they sent out scary email to phish people**
  - States an update is required for one of the users key programs
  - Popup looks similiar to that of when authentication to proxy server is required
  - They entered in their Username + Passwords
  - Got 45/150 personal details 
  - After they entered details and click okay a nice little load bar come up to hide any attention

**Kiosks:**
  - Break out of applications in kiosk by browsing to any site that allows you to pop up a file explorer in the browser (upload file etc)
  - Meterpreter is awesome to utilise

**XOR signatures can potentially bypass**
  - The Deloitte team doesn't like using Metasploit Framework (MSF) due to it’s simplicity and lack of further developing their teams skill sets, they only use MSF on time restricted engagements, from a learning perspective going through the code and how it works is far more beneficial (NOTE: Don't just copy and paste as trolls add rm/rf commands to delete system files wiping device)
  - Always look at the exploit you’re going to run as there are dangerous commands and scripts in files

**Famous technique, easy to detect though**
Break out security system by:
  - Use browser to navigate to file explorer to open cmd
  - Run an .exe in full path it will try open it up as correct 
  - Open up local privilege escalation exploit
  - Run mimicats to download all clear text credentials from memory
  - Running netsc in cmd then login as administrator
  - This will now log into the citrix system so it will now go to citrix admin system

**Red Team Operations**
  - Name came from a military context
  - Highly skilled penetration testers working towards a set predefined goal
  - Different missions involved include either Physical access, System Access, Social engineering etc or a mix of all
  - Simulates how a real world attacker will gain access to the system
  - Need to do a virtual map of all aspects, rooms/security features+location/weapons used/external features/internal features/patterns/look like you belong there/act confident and go in, utilise a rubber ducky to do a reverse shell exploit within building and ALWAYS BE PREPARED TO BE QUESTIONED

**Traditional**
  - Specific
  - Limited Scope
  - Narrow

**Realistic approach to security testing**
  - Realistic
  - Relevant
  - Readiness

**Tools used:**
  - RFID scanner/duplicator (check what type of cards they use, put scanner in iPad sized case/brush past target utilising crowded places as they are less likely to take note of you when bumping into/past them)
  - Lock picks (3 pin locks used on some old ATMs, can be picked within 3 seconds)
  - PwnPlug (power + corp Ethernet – utilised as an extender to do port forwarding allowing SSH tunnel and what you control, from home office can connect into their network GLAR150 + 4G dongle + optional open-boards OS)
  - PowerPwn variant
  - Wifi-Pinapple (Creates fake hot spots replicating corporate network Access Points)
  - Rubber Ducky (simulates a keyboard), Feed scripts into micro SD card, plug it in and it will do everything you want to do quickly (Run \\etc)
  - Physical hardware testing (i.e. router has pins on board, just need to figure out the different pins and connect via usb-pin adapter to a laptop, UART)
  - Kali OS/Metasploit Framework/Powershell Empire/etc


**Introductory programs offered**
GRADUATE PROGRAM/VOCATIONAL PROGRAM
(Full-time & Part-time roles available)
  - Cyber department has family/team environment
  - Cyber Intelligence Centre (Incident Response, Pentesting, Red Teaming, Breaking stuff in general)
  - Generally starts off in monitoring and proceeded onto Pen-testing etc
  - Reach out to them for contact details
  - Your future.deloitte.au
  - First year get to work with everything (multiple divisions)
  - Certifications are paid for
  - Go straight into Analyst work while also having professional consultant training in soft skills + your technical skills

**Question Asked**:
I asked what the average daily hours are for Graduate workers in Deloitte's Cyber
  - Typical work day is 9am-5:30pm, though some divisions are on a 24/7 rotational roster

I also asked what modes of employment they offer
  - Both full-time and part time roles are available for Graduates.

They also stated that they don’t expect us to be immediately pros – they like to teach you the correct ways, they are strong believers in continuous education and up-skilling.

Artifact: got all three of their email addresses.



### **My presentation excerpt**
[Cover Page](https://github.com/AlwaysExtreme/root9b/blob/master/screenshots/PresentationArtifact.png)

(TITLE SLIDE)

Good afternoon,

My name is Mitchell and today myself, Max & Harry are going to talk to you about the infamous password cracker, “John the Ripper”.

(NEXT SLIDE)

What is John the Ripper?

(CLICK)

That is an excellent question!

(NEXT SLIDE)

If you’re thinking infamous serial killer John the Ripper, (CLICK) you’d be wrong, though they do hold two things in common, their notoriousness and their ability to kill… passwords in our case.

(NEXT SLIDE)

John the Ripper is a password cracking tool that has been cracking around as a prototype since 1995 and officially released for DOS in 1996. Since its introduction, it has cracked billions of passwords at lightning fast speeds and been taken over and continuously improved by Openwall.

(NEXT SLIDE)

For enthusiasts, there is also a community Jumbo version hosted on GitHub for people to commit too, but this isn’t as high quality or bug proof as the free & pro versions developed by Openwall. 

(NEXT SLIDE)

At current, it supports 15 different platforms including Windows and many distros of unix, there is no bias here (CLICK), it’s one of the most popular password testing and breaking tools as it combines multiple password crackers into a single package including a fully customisable version, while also providing features such as auto-detection of password hash types.

(NEXT SLIDE)

As mentioned in the previous slide, out of the box, it can auto-detect & run numerous types of plaintext & encrypted/hashed (CLICK) password formats such as:
  - Unix crypt(3) hash types: 
  - Traditional DES-based
  - Bigcrypt 
  - BSDI extended DES-based
  - FreeBSD MD5-based (used in Linux & Cisco IOS)
  - OpenBSD Blowfish-based (used in recent versions of Linux distros and Solaris)
  - Kerberos/AFS
  - Windows LM (DES-based) hashes and
  - DES-based tripcodes

John the Ripper uses three types of password attacks, these are:
  - Dictionary Attacks
  - Brute Force Attacks
  - And my favorite - Rainbow Tables

Which I picture look a bit like this.. (CLICK)

But I’ll let Harry go into further details about these.


## Thursday
  - I worked 9am-5:30pm in my IT Support Role.
  - Migrated website over to new Domain. 
  - Worked on Deloitte VM

### My Domain Migration Details:
[Link to Domain Setup](https://root9b.tech/2019/02/22/Domain-Migration.html)


## Friday
**Pentesting Part 1 - Deloitte VM**

**Pentesting Part 2 - Authorised Website Analysis**

[Link to Writeups](https://root9b.tech/2019/02/15/CTF.html)


## Saturday
  - I worked 9am-5:30pm in my IT Support Role
  - Further modified numerous Cloudflare settings including Security and Optimisation.
  - Worked on Reflection for Sunday.

## Sunday
  - I worked 9am-5:30pm in my IT Support Role
  - Upon arriving home, I find that my website had gone down due to a SSL certificate for my website had been broken by my DNS provider so had to message their support team to look into the issue. 



# Reflection

This week we jumped into doing physical penetration testing of systems with the goal of going from Boot to Root. This was quite a step up again from the previous week, as we had to utilise multiple different skills with a creative mindset to exploit networks (protocols) and applications in ways that they had never been intended for so that we could gain illicit access to the target system with the purpose of gaining full control of it, otherise known as "Root"access.

**Monday** in Scrum, Riley identified that there is a lack of security in the software development lifecycle, and when patches do become available for these, many people don't even update to the latest version. He also identified how readily available hacking content is and how it has pros (those aspiring to be white hat hackers) and cons (content is available to Black hat hackers; due to the amount of content available it inhibits the research process).

Riley and I had seemed to not quite grasp onto the concepts of programming/scripting taught to us in the university programming classes. Perhaps there is a need to change the processes of the way these classes are taught from the strict "must do what we say" criteria, to something that aids the student in their end goal in their particlar language/languages and have them create a project in their language of choice developing something they want to, as motivation and success in learning comes from an addictive interest to create.

At home, I started to research John the Ripper and put my notes together. I found that John the Ripper had far less information on it then other offensive toolsets but the information provided for it was detailed enough to explore. This was quite an interesting learning experience which I enjoyed developing over the following days.

On  **Tuesday**, my group and I utilised Microsoft Teams and Google Docs PowerPoint to prepare for the presentation on Wednesday. I found that even though we were apart, we were effectively able to communicating between each other and utilising the planner to achieve our goals on time.

**Wednesday** was rather quite an educational day especially with the Industry Professionals from Deloittes Cyber Security team giving their presentation and providing us with a target VM to penetrate. I gained a deep insight into the offensive security industry and found that I really like the sound of Red Teaming, it sounds exciting. With being able to engage in conversation with the Deloitte staff, I was able to have key questions answered regarding job rolls, progression and tips for gaining an entry level role in security. I was also able to gather their contact details if ever I have a question to ask them.

In my presentation that afternoon, I was able to further improve my communication and presentation skills. I feel like I was much bettrer prepared this time round, though I feel that I still relied on my palm cards too much. This is something I will need to continue to improve on [John The Ripper - Meme](https://github.com/AlwaysExtreme/root9b/blob/master/screenshots/JohnTheRipperVsPasswords.png).

That night I researched further into what was required to migrate over to my new domain from the Github hosted pages, it was easier than I thought to do and I had prepared everything before going to bed, as preperation is key to minimising downtime.

After work on **Thursday** I migrated my website across to the new domain within an hour, I spent another hour configuring some additional settings to how I wanted them. I found this migration quite interesting as I had never quite understood the process for creating a website, creating a domain and then combining the two. This will prove invaluble in the future.

After the successful migration, I spent the remainder of the night working on Deloittes VM, after many hours of trouble shooting and thinking outside of the box I was able to gain User Access to the machine via SSH. I need to learn how to then gain access from user to root as this is where I got stuck[User Access Via SSH](https://github.com/AlwaysExtreme/root9b/blob/master/screenshots/UserAccessViaSSH.png).

**Friday** morning I continued on with the Deloitte VM before changing my focus onto the website I had been given permission to test. I was able to run a scan using ZAP to identify potential vulnerabilities in the websites defences. I'd like to learn how to safely further these advances on the website as to demonstrate these vulnerabilities being exploited, and seeing what an attacker could have gained access too. Once I have achieved this I'd love to write a report on how they can secure these vulnerabilites, but I will leave this until I increase my knowledge in this field [Link to Writeups](https://root9b.tech/2019/02/15/CTF.html).

On **Saturday**, I modified numerous Cloudflare settings including those regarding Security and Optimisation. This would prove to be troublesome in the coming days due to an SSL certificate [Link to Domain Setup](https://root9b.tech/2019/02/22/Domain-Migration.html). I also began working on this reflection where I started to identify loose ends that I had not yet completed, which I resolved during my lunch break at work on Sunday.

**Sunday** was by far the most troublesome day, not only did I need to complete unfinished work and have this reflection due, but when I had got hope I found my website had gone down and by the time i'm writing this had spent hours troubleshooting the issue [SSL-DOWN](https://github.com/AlwaysExtreme/root9b/blob/master/screenshots/SSLCertificateError.png). I ended up having to temporarily deactivate some of Cloudflares security settings due to the SSL Certificate being invalid, which still allowed for SSL to be enabled but not for it to be strengthened. This brought my website back up but this will need to be investigated further in the coming days.

Overall this week i'm quite proud of how far i've come and the personal achievements that i've gained, I feel that this course has helped me develop the technical skills i've been so longing to attain. Being among a group of people with the same interest in Cyber Security has only furthered the friendships and learning experience.

Next week I hope to learn more about the Boot2Root process and potentially implement reverse engineering into the process that i'm currently utilising, in the hope that when it comes to CySCA2019 i'm able to tackle these rarely touched areas of expertice.


# Useful resources
  - [Exploit-DB](https://www.exploit-db.com/)
  - [Kali Revealed](https://kali.training/downloads/Kali-Linux-Revealed-1st-edition.pdf)
  - [SSL Analyser](https://sslanalyzer.comodoca.com/)
  - [DNS Visuliser](http://dnsviz.net/)


## [SPRINT 4 LINK](https://root9b.tech/2019/02/25/Sprint-4-Retrospective.html)

---
Please feel free to [contact me via email](mailto:mitchell.l.tuck@student.uts.edu.au) if you have any questions.

<!--more-->

---
