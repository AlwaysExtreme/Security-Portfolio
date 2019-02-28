---
# title: "Submission 2: Cyber Security: An Offensive Mindset"
tags: Cybersecurity, UTS, Summer-Studio, Cyber-Security-An-Offensive-Mindset, Sprint-2

---
# SPRINT 2 - Web Application Security


# Problem statement
I want to go from having theoretical knowledge of Web Application Security to being able to utilise WAS in a practical environment, to find and notify vulnerable parties.



# Bug Bounties
Every piece of technology ever developed or that ever will be developed will contain some form of bug, whether they are part of poorly written code or arise in future updates or integration with other code (such as plugins etc), there will always be bugs. Ethical hacking and Bug Bounties have changed the way businesses have approached these security threats in multiple ways. This can be broken down into two different impact vectors, these being:

## Positives
  - Allowing freelance security researches to find and notify vulnerable parties of potential vectors of attack/s in their software
  - Being a proactive security measure protecting companies and their customers
  -	Building further security awareness and transparency towards stakeholders
  -	Giving peace of mind knowing there is additional help in protecting stakeholders

## Negatives
  -	Full disclosure can put strain on DevOps 
  -	Full disclosure can put strain on PR teams
  -	If not fixed immediately can lead to a bad press potentially affecting stock market shares
  -	Potential legal action can be taken if proof a company has been notified of a vulnerability but had done nothing about it before a breach
  - Ultimately loss of faith with a company and shareholders dispersing elsewhere


___
# Utilising a Responsible Disclosure program with this weeks Web application Security
Through researching documentation such as Bugcrowds open sourced responsible disclosure policy [Artifact 1: Disclosure Policy](https://github.com/bugcrowd/disclosure-policy), and joining a bug bounty program, I can implement my new-found knowledge of XSS + SQL to test vulnerable sites which can be found by using resources such as Google Dorks searches (inurl:.com/search.asp or further customised) to narrow down potential targets. 

I have also found that it's not recommended to use something which states an “alert” with random text via the script but rather it should be written as "alert(document.domain)" or similar for the administrators. An example of this would be the pop-up seen upon arrival to this page of mine (reload page to see Artifact 2 again), that script is located here: (invisible) <script>alert("Artifact 2 - Remember this pop-up for later..");</script> but states: </script/>alert(“Artifact 2 - Remember this popup for later..”);</script/>. This is useful for this demonstartion but not useful for the developers who need to patch the issue.


## What you can do: -
Follow all rules laid out by the company in question, specifically:
  - [Website URI]
  - [Product Information]
  - [Additional Details]

## What you cannot do: -

    - 3rd Party Services
    - Findings from physical testing such as office access (e.g. open doors, tailgating)
    - Findings derived primarily from social engineering (e.g. phishing, vishing)
    - Findings from applications or systems not listed in the ‘Scope’ section
    - UI and UX bugs and spelling mistakes
    - Network level Denial of Service (DoS/DDoS) vulnerabilities


___
# Practical Experiment
PentesterLab - XSS and MySQL FILE

  1) Configuring xss_and_mysq Virtual Machine with IP 192.168.44.44 (hosts the vulnerable website):
  
   [Artifact 1: Conguring VM](https://github.com/AlwaysExtreme/root9b/blob/master/screenshots/XSSSQLi1.png)


  2) Proof server can reach attacking machine:
  
   [Artifact 2: Connection Confirmed](https://github.com/AlwaysExtreme/root9b/blob/master/screenshots/XSSSQLi2.png)


  3) Accessing a vulnerable website through Kali Linux Virtual Machine

   [Artifact 3: Open Webpage](https://github.com/AlwaysExtreme/root9b/blob/master/screenshots/XSSSQLi3.png)


  4) Checking if post allows for the execution of code on a server:

   [Artifact 4: Code Execution Test](https://github.com/AlwaysExtreme/root9b/blob/master/screenshots/XSSSQLi4.png)


  5) The result shows that it does, “Test!” is now H1 size:

   [Artifact 5: Code Test Confirmed](https://github.com/AlwaysExtreme/root9b/blob/master/screenshots/XSSSQLi5.png)


  6) Now to see if scripts will execute: 

   [Artifact 6: Script Execution Test](https://github.com/AlwaysExtreme/root9b/blob/master/screenshots/XSSSQLi6.png)


  7) We have success!

   [Artifact 7: Script Test Confirmed](https://github.com/AlwaysExtreme/root9b/blob/master/screenshots/XSSSQLi7.png)


  8) Checking for cookies:

   [Artifact 8: Cookies](https://github.com/AlwaysExtreme/root9b/blob/master/screenshots/XSSSQLi8.png)


  9) Successful: for the administrator, it would also show their username and password here, this is not too useful for an external attacker:

   [Artifact 9: XSS Success](https://github.com/AlwaysExtreme/root9b/blob/master/screenshots/XSSSQLi9.png)


___
# Friday Deliverable – Presentation to Stakeholder

Good evening,

This week I decided that I wanted to expand on my theoretical knowledge of Web Application Security and utilise it in a practical environment within tight time constraints, thus to find and notify vulnerable parties on the day same day of identification.
I found your website participating in a bug bounty program and decided to investigate your website for potential vulnerabilities (in scope of the BugBounty) which identified that I was able to manipulate the content of your website by using Cross Site Scripting (XSS) & SQL Injection.

This permitted me to capture the cookies of the administrator allowing me to load the administrators session gaining me direct access to your website. Once in, there was further ability to utilise SQL injections for further code execution which could be used for retrieving sensitive information from your servers.

First, the Cross-Site Scripting vulnerability allowed me to gain access to the administration pages. Once in the "Trusted zone", more functionalities become available to me which lead to further vulnerabilities being identified. Using the fact that the MySQL user had high privileges within the system it allowed me to gain code execution privileges on the server by deploying a Web Shell through an SQL injection.

These vulnerabilities will affect your company drastically if found by an aggressor as it allows direct access to sensitive information. The impacts of this if exploited by a malicious actor will severely affect your company:
    - Financially
    - Reputationally
    - And hold further legal consequences to you as a key stakeholder & the company as a whole (i.e. prosecution by a court of law with fines & potential imprisonment)
    
It is crucial that security is met at every aspect of the software development life-cycles to prevent issues like this from happening in the future. These current vulnerabilities can be mitigated by preventing the ability of external users from being able to post to your website or set up restrictions on what can be posted. 

Another is by lowering privileges of the user by blocking code execution on the website thus slowing down an aggressor, limiting the compromise of your databases. I can provide further detailed information on ways to secure your website while discussing the responsible disclosure of information policy with you. 

Thank you for your time.


___
# Problem Statement Refined:
Utilising the OWASP Top 10 Web Application Security Risks, employ XSS and SQLi in a practical environment.
___


# SPRINT 2 - REFLECTION

During week two of Summer Studio 2019, Sprint 2 of the agile methodology was focused on Application Security.

We had an industry expert named Luke Fuehrer give a presentation and engage us in technical conversation. Luke works in a Red Team whose purpose is to penetrate into companies as if they were a malicious actor to highlight key vulnerabilities to a company allowing them to patch it before an actual malicious party exploits the vulnerability.

He spoke about when Cross-Site Scripting (XSS) first come to light, it was classed as a “lame” vulnerability due to its prevalence across the internet and indirect use for a hacker to achieve their goal. In the modern era, this "lame" vulnerabilities is now part of a "kill chain" to take something down. He mentioned how is very rare for just one form of attack to be used to engage a target and how it's generally multiple attack methods combined to form the perfect offensive.

In his presentation, he stated that in his opinion XSS is the number one vulnerability as it opens up a lot of avenues to further exploit. The moment you allow a user to have some form of input on a website, there is a huge increase in vulnerability that comes with this. XSS has been used to compromise high-profile organisations allowing for exfiltration of confidential data costing the company their reputation and impacting them financially.

It was brought to my attention that XSS represents a critical security weakness within an application with the vast majority of black hat hackers using simplistic attack methods/exploits such as this to cause severe damage to vulnerable parties. With its ability to also be manipulated to distribute Viruses & Worms it proves to be a very good vector of attack.

## Luke stated that there are three varieties of XSS:
***Reflected***
Most common with ~75% of all XSS being Reflected, this is where a request containing embedded JavaScript that is reflected to any user who makes the request, attack payload is then delivered and executed through a single request and response. Any time you rely on user input as mentioned above, it becomes a risk as it’s directly changing code stored on a site.

***Stored***
Happens when data submitted by a user is stored in the application (back-end-DB) and then is displayed to others without filtered or sanitised appropriately.

***DOM-based***
User requests crafted URL supplied by attacker containing embedded JavaScript, Server response (Browsers Document Object Model (DOM)), a portion of the browser is now running as JavaScript etc in memory, it’s no longer just HTML/CSS, hence why browsers are so resource heavy. Trackers are an example of this which utilise this to track what is being searched and presenting adverts relevant to you as a person. 

It’s recommended to utilise a plugin called Ghostery or uBlockOrigin to prevent/stop and notify the user of current trackers to protect the users' security, also useful to see what websites are tracking of the user.

## XSS research case study: eBay’s Stored XSS Vulnerability
This attack was where persistent cross-site scripting vulnerabilities were utilised to steal account credentials, this wasn’t the first case either as there were a string of attacks previously to this event. Many of the listings that had been exploited had remained on eBay's website for more than a month before they were eventually removed. It was basically a MITM attack utilising XSS to grab confidential user details and redirect them to similar but fraudulent listings.

This could have been mitigated by limiting active content (such as JavaScript), before eventually blocking it altogether. If this is implemented as a technical control (for example, by using iframes with Content Security Policy and sandbox restrictions), then such attacks should become impossible to carry out against modern browsers in the future (Netcraft 2017).

In my presentation where I communicated to the class as if they were the shareholder, I was able to communicate clearly and effectively keeping them actively listening. Larry told me that I needed to be more concise with my problem statement which has since been cleaned up.

During the scrum meetings, I was able to communicate with my peers regarding what we had done during the week, what we planned to do for the week ahead and what were our roadblocks. In my group, there were mixed opinions but one thing stood out and that was there was a need for a focus on the practical side of penetration testing so that we could be more effective in the industry.

During the penetration testing of the PentesterLabs virtual machine, all went smooth until I got to the SQL Injection (SQLi), I could see that there was an ability to call certain datasets from the database, just I had issues with understanding what needed to be written to retrieve the data. In the coming week, I want to build upon this to further fortify my SQLi knowledge.

This week has been rather quite interesting and I have learned a great deal regarding Application Security, I hope to expand on this knowledge and meet my problem statement in the coming week.

***Further keynotes I learned this week:***

    - With using so many different applications it can be hard to keep track of all of the commands, thus it is necessary to keep them all in one place in a document such as Notepad++ or similar.
    
    - Priority is to do research first, then do the practical side followed by write-ups to remember how it was achieved.
    
    - When speaking to an Executive or Stakeholder, need to state at the beginning what happens at the end to GRAB THEIR attention within the first 30 seconds.


# Issues

I had a problem with the SQL part of the box I was penetrating due to a low level of SQL understanding, this is something that I need to further develop on so that I am able to pass this hurdle in future penetration testing.

___
# References

Bugcrowd 2018, *disclosure-policy?*, San Francisco, viewed 14 February 2019, <<https://github.com/bugcrowd/disclosure-policy>>.

Bugcrowd 2018, *What is Responsible Disclosure?*, San Francisco, viewed 14 February 2019, <<https://www.bugcrowd.com/resource/what-is-responsible-disclosure/>>.

Exploit Database 2019, *Exploits for Penetration Testers, Researchers, and Ethical Hackers*, Online, viewed 15 February 2019, <<https://www.exploit-db.com/>>.

Exploit Database 2019, *Google Hacking Database*, Online, viewed 15 February 2019, <<https://www.exploit-db.com/google-hacking-database>>.

Google 2019, *When reporting XSS, don't use alert(1) - Bughunter University*, Online, viewed 16 February 2019, <<https://sites.google.com/site/bughunteruniversity/improve/alert-1-considered-harmful>>.

Hackerone 2018, *Vulnerability Disclosure Guidelines*, San Francisco, viewed 15 February 2019, <<https://www.hackerone.com/disclosure-guidelines>>.

Hacking-tutorial 2013, *XSS Attack: Finding Simple XSS Vulnerability*, Online, viewed 14 February 2019, <<https://www.hacking-tutorial.com/hacking-tutorial/xss-attack-finding-simple-xss-vulnerability/#sthash.DwtxUkUF.dpbs>>.

Netcraft 2017, *Hackers still exploiting eBay’s stored XSS vulnerabilities in 2017*, Online, viewed 16 February 2019, <<https://news.netcraft.com/archives/2017/02/17/hackers-still-exploiting-ebays-stored-xss-vulnerabilities-in-2017.html>>.

Offensive Security 2017, *Kali Linux Revealed*, viewed 15 Feburary 2019, <<https://kali.training/downloads/Kali-Linux-Revealed-1st-edition.pdf>>.



---
Please feel free to [contact me via email](mailto:mitchell.l.tuck@student.uts.edu.au) if you have any questions.

<!--more-->

---
