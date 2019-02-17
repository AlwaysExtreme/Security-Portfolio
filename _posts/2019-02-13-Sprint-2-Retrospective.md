---
# title: "Submission 2: Cyber Security: An Offensive Mindset"
tags: Cybersecurity, UTS, Summer-Studio, Cyber-Security-An-Offensive-Mindset, Sprint-2

---
# Problem statement
I want to go from having theoretical knowledge of Web Application Security to being able to utilise WAS in a practical environment, to find and notify vulnerable parties.



# Bug Bounties
Every piece of technology ever developed or that ever will be developed will contain some form of bug, whether they are part of poorly written code or come arise in future updates or integration with other code (such as plugins etc), there will always be bugs. Ethical hacking and Bug Bounties have changed the way businesses have approached these security threats in multiple ways. This can be broken down into two different impact vectors, these being:

## Positives
  - Allowing freelance security researches to find and notify vulnerable parties of potential vectors of attack/s in their software
  - Being a proactive security measure protecting companies and their customers
  -	Building further security awareness and transparency towards stakeholders
  -	Giving piece of mind knowing there is additional help in protecting stakeholders

## Negatives
  -	Full disclosure can put strain on DevOps 
  -	Full disclosure can put strain on PR teams
  -	If not fixed immediately can lead to a bad press potentially effecting stock market shares.
  -	Potential legal action can be taken if proof a company has been notified of a vulnerability but had done nothing about it before a breach.
  - Ultimately loss of faith with a company and shareholders dispersing elsewhere



# Utilising a Responsible Disclousre program with this weeks Web application Security
Through researching documentation such as Bugcrowds open sourced responsible disclosure policy https://github.com/bugcrowd/disclosure-policy (Artifact 2), and joining a bug bounty program, I can implement my new-found knowledge of XSS + SQL to test vulnerable sites which can be found by using resources such as Google Dorks searches (inurl:.com/search.asp or further customised) to narrow down potential targets. 

I have also found that it's not recommended to use something which states an “alert” with random text via the script but rather it should be written as "alert(document.domain)" or similar for the administrators. An example of this would be the pop-up seen upon arrival to this page of mine (reload page to see Artifact 1 again), that script is located here: (invisible) <script>alert("Artifact 1 - Remember this pop-up for later..");</script> but states: </script/>alert(“Artifact 1 - Remember this popup for later..”);</script/>. This is useful for this demonstartion but not useful for the developers who need to patch the issue.


### What you can do: -
Follow all rules layed out by the company in question, specifically:
  - [Website URI]
  - [Product Information]
  - [Additional Details]

### What you cannot do: -

    - 3rd Party Services
    - Findings from physical testing such as office access (e.g. open doors, tailgating)
    - Findings derived primarily from social engineering (e.g. phishing, vishing)
    - Findings from applications or systems not listed in the ‘Scope’ section
    - UI and UX bugs and spelling mistakes
    - Network level Denial of Service (DoS/DDoS) vulnerabilities


# Practical Experiment
PentesterLab - XSS and MySQL FILE

Configuring xss_and_mysq Virtual Machine with IP 192.168.44.44 (hosts the vulnerable website):
![](/screenshots/2019-02-13 21_45_49-Debian 6 - xss_and_mysq - VMware Workstation.png)
        
      


Proof server can reach attacking machine:
(IMAGE HERE)


Accessing vulnerable website through Kali Linux Virtual Machine
(IMAGE HERE)

Checking if post allows for execution of code on server:
(IMAGE HERE)

Result shows that it does, “Test!” is now H1 size:
(IMAGE HERE)

Now to see if scripts will execute: 
(IMAGE HERE)

We have success!
(IMAGE HERE)

Checking for cookies:
(IMAGE HERE)

Successful: for the administrator it would also show their username and password here, this is not too useful for an external attacker:
(IMAGE HERE)



FRIDAY DELIVERABLE – PRESENTATION OF VULN TO STAKEHOLDERS

Thank you for your time,

This week I decided that I wanted to expand on my theoretical knowledge of Web Application Security and utilise it in a practical environment within tight time constraints, thus to find and notify vulnerable parties on the day same day of identification.
I found your website participating in a bug bounty program and decided to investigate your website for potential vulnerabilities (in scope of the BugBounty) which identified that I was able to manipulate the content of your website by using Cross Site Scripting (XSS) & SQL Injection.

This permitted me to capture the cookies of the administrator allowing me to load the administrators session gaining me direct access to your website. Once in, there was further ability to utilise SQL injections for further code execution which could be used for retrieving sensitive information from your servers.

First, the Cross-Site Scripting vulnerability allowed me to gain access to the administration pages. Once in the "Trusted zone", more functionalities become available to me which lead to further vulnerabilities being identified. Using the fact that the MySQL user had high privileges within the system it allowed me to gain code execution privileges on the server by deploying a Web Shell through an SQL injection.

These vulnerabilities will affect your company drastically if found by an aggressor as it allows direct access to sensitive information. The impacts of this if exploited by a malicious actor will severely affect your company:
    - Financially
    - Reputationally
    - And hold further legal consequences to you as a key stake holder & the company as a whole (i.e. prosecution by a court of law with fines & potential imprisonment)
    
It is crucial that security is met at every aspect of the software development life-cycles to prevent issues like this from happening in the future.

These current vulnerabilities can be mitigated by preventing the ability of external users from being able to post to your website or set up restrictions on what can be posted. 

Another is by lowering privileges of the user by blocking code execution on the website thus slowing down an aggressor, limiting the compromise of your databases. I can provide further detailed information on ways to secure your website while discussing the responsible disclosure of information policy with you. 
Thank you.

### I have since updated my problem statement too:
Utilising the kowledge provided in the OWASP Top 10 Web Application Security Risks, employ XSS and SQLi in a practical environment.








# Useful Links: (MAKE THESE UTS HARVARD STYLE REFERENCING?????????????????????????????)
https://www.hackerone.com/disclosure-guidelines

https://www.bugcrowd.com/resource/what-is-responsible-disclosure/

https://github.com/bugcrowd/disclosure-policy

https://www.hacking-tutorial.com/hacking-tutorial/xss-attack-finding-simple-xss-vulnerability/#sthash.DwtxUkUF.dpbs

https://kali.training/downloads/Kali-Linux-Revealed-1st-edition.pdf

https://www.exploit-db.com/

https://www.exploit-db.com/google-hacking-database

https://sites.google.com/site/bughunteruniversity/improve/alert-1-considered-harmful

---
Please feel free to [contact me via email](mailto:mitchell.l.tuck@student.uts.edu.au) if you have any questions.

<!--more-->

---
