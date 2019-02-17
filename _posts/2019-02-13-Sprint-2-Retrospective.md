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
  -	If not fixed immediately can lead to a bad press potentially effecting stock market shares
  -	Potential legal action can be taken if proof a company has been notified of a vulnerability but had done nothing about it before a breach
  - Ultimately loss of faith with a company and shareholders dispersing elsewhere



# Utilising a Responsible Disclousre program with this weeks Web application Security
Through researching documentation such as Bugcrowds open sourced responsible disclosure policy [Artifact 1: Disclosure Policy](https://github.com/bugcrowd/disclosure-policy), and joining a bug bounty program, I can implement my new-found knowledge of XSS + SQL to test vulnerable sites which can be found by using resources such as Google Dorks searches (inurl:.com/search.asp or further customised) to narrow down potential targets. 

I have also found that it's not recommended to use something which states an “alert” with random text via the script but rather it should be written as "alert(document.domain)" or similar for the administrators. An example of this would be the pop-up seen upon arrival to this page of mine (reload page to see Artifact 2 again), that script is located here: (invisible) <script>alert("Artifact 2 - Remember this pop-up for later..");</script> but states: </script/>alert(“Artifact 2 - Remember this popup for later..”);</script/>. This is useful for this demonstartion but not useful for the developers who need to patch the issue.


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

  1) Configuring xss_and_mysq Virtual Machine with IP 192.168.44.44 (hosts the vulnerable website):
  
   [Artifact 1: Conguring VM](root9b/screenshots/XSSSQLi1.png)


  2) Proof server can reach attacking machine:
  
   [Artifact 2: Connection Confirmed](root9b/screenshots/XSSSQLi2.png)


  3) Accessing vulnerable website through Kali Linux Virtual Machine

   [Artifact 3: Open Webpage](root9b/screenshots/XSSSQLi3.png)


  4) Checking if post allows for execution of code on server:

   [Artifact 4: Code Execution Test](root9b/screenshots/XSSSQLi4.png)


  5) Result shows that it does, “Test!” is now H1 size:

   [Artifact 5: Code Test Confirmed](root9b/screenshots/XSSSQLi5.png)


  6) Now to see if scripts will execute: 

   [Artifact 6: Script Execution Test](root9b/screenshots/XSSSQLi6.png)


  7) We have success!

   [Artifact 7: Script Test Confirmed](root9b/screenshots/XSSSQLi7.png)


  8) Checking for cookies:

   [Artifact 8: Cookies](root9b/screenshots/XSSSQLi8.png)


  9) Successful: for the administrator it would also show their username and password here, this is not too useful for an external attacker:

   [Artifact 9: XSS Success](root9b/screenshots/XSSSQLi9.png)



# Friday Deliverable – Presentation to Stakeholder

Good evening,

This week I decided that I wanted to expand on my theoretical knowledge of Web Application Security and utilise it in a practical environment within tight time constraints, thus to find and notify vulnerable parties on the day same day of identification.
I found your website participating in a bug bounty program and decided to investigate your website for potential vulnerabilities (in scope of the BugBounty) which identified that I was able to manipulate the content of your website by using Cross Site Scripting (XSS) & SQL Injection.

This permitted me to capture the cookies of the administrator allowing me to load the administrators session gaining me direct access to your website. Once in, there was further ability to utilise SQL injections for further code execution which could be used for retrieving sensitive information from your servers.

First, the Cross-Site Scripting vulnerability allowed me to gain access to the administration pages. Once in the "Trusted zone", more functionalities become available to me which lead to further vulnerabilities being identified. Using the fact that the MySQL user had high privileges within the system it allowed me to gain code execution privileges on the server by deploying a Web Shell through an SQL injection.

These vulnerabilities will affect your company drastically if found by an aggressor as it allows direct access to sensitive information. The impacts of this if exploited by a malicious actor will severely affect your company:
    - Financially
    - Reputationally
    - And hold further legal consequences to you as a key stake holder & the company as a whole (i.e. prosecution by a court of law with fines & potential imprisonment)
    
It is crucial that security is met at every aspect of the software development life-cycles to prevent issues like this from happening in the future. These current vulnerabilities can be mitigated by preventing the ability of external users from being able to post to your website or set up restrictions on what can be posted. 

Another is by lowering privileges of the user by blocking code execution on the website thus slowing down an aggressor, limiting the compromise of your databases. I can provide further detailed information on ways to secure your website while discussing the responsible disclosure of information policy with you. 

Thank you for your time.



# Problem Statement Refined:
Utilising the kowledge provided in the OWASP Top 10 Web Application Security Risks, employ XSS and SQLi in a practical environment.



# Reflection
??Intro

??Try meet all 5 SLOs, if can't meet all explain why the ones not included couldn't be done
??Use sheets provided last week for help
??Check if any sheets available for this week?

??conclusion

# SPRINT 2 - REFLECTION

During week two of Summer Studio 2019, Sprint 2 of the agile methedology was focused on Application Security.

We had a industry expert named Luke Fuehrer give a presentation and engage us in technical conversation. Luke works in a Red Team whos purpose is to penetrate into companys as if they were a malicious actor to highlight key vulnerabilities too a company allowing them to patch it before an actual malicious party exploits the vulnerability.

He spoke about when Cross-Site Scripting (XSS) first come to light, it was classed as a “lame” vulnerability due to it’s prevalence across the internet and indirect use for a hacker to achieve their goal. In the modern era this "lame" vulnerability is now part of a "kill chain" to take something down. He mentioned how is very rare for just one form of attack to be used to enegage a target and how it's generally multiple attack methods combined to form the perfect offensive.

???????

Today XSS is seen as the number 1 vulnerability
The moment you allow a user to have some form of input on a website, there is a huge increase in vulnerability you bring. XSS has been used to compromise high-profile organisations allowing for exfiltration of confidential data from that company
XSS represents a critical security weakness within an application.
Vast majority of black hat hackers are using simplistic attack methods/exploits
It can be combined with other vulnerabilities to be very destructive
XSS can also be manipulated to distribute Viruses & Worms

Session token
Hidden field

XSS is a Swiss-Army knife


Three varieties of XSS:
Reflected
Common (75% of all XSS Vulns) 
Taking a request containing embedded JavaScript that is reflected to any user who makes the request, attack payload is then delivered and executed through a single request & response.
Any time you rely on user input as mentioned above, it becomes a user as it’s directly changing code stored on a site
First order XSS injection (using
Stored
Happens when data submitted by a user is stored in the application (back-end-DB) and then is displayed to others without filtered or sanitised appropriately.
Second step order XSS injection

DOM-based
User requests crafted URL supplied by attacker containing embedded JavaScript
Server response (Browsers Document Object Model (DOM))
Portion of browser is now running as JavaScript etc in memory, it’s no longer just HTML/CSS, hence why browsers are so resource heavy. Trackers are an example of this which utilse this to track what is being searched and presenting adverts relevant to you as a person. It’s recommended to utilise a plugin called Ghostery/uBlockOrigin to prevent/stop and notify the user of current trackers to protect the users security, useful to see what 




# References
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
