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
How you can implement things you've learnt throughout the week to test web apps under a responsible disclosure program
Through researching documentation such as Bugcrowds open sourced responsible disclosure policy https://github.com/bugcrowd/disclosure-policy, and joining a bounty program, I can implement my new-found knowledge of XSS + SQL to test vulnerable sites which can be found by using resources such as Google Dorks (inurl:.com/search.asp or further customised) to narrow down potential targets. It is not recommended to use something which states “alert” as it can send alarm bells, an example of this would be the pop-up seen upon arrival to this site (reload page to see again), that script is located here: (invisible) <script>alert("Artifact 1 - Remember this pop-up for later..");</script> but states: </script/>alert(“Artifact 1 - Remember this popup for later..”);</script/>.
https://sites.google.com/site/bughunteruniversity/improve/alert-1-considered-harmful

### What you can do: -
  - [Website URI]
  - [Product Information]
  - Additional Details

### What you cannot do: -

    - 3rd Party Services
    - Findings from physical testing such as office access (e.g. open doors, tailgating)
    - Findings derived primarily from social engineering (e.g. phishing, vishing)
    - Findings from applications or systems not listed in the ‘Scope’ section
    - UI and UX bugs and spelling mistakes
    - Network level Denial of Service (DoS/DDoS) vulnerabilities


# Bibliography:
https://www.hackerone.com/disclosure-guidelines
https://www.bugcrowd.com/resource/what-is-responsible-disclosure/
https://github.com/bugcrowd/disclosure-policy
https://www.hacking-tutorial.com/hacking-tutorial/xss-attack-finding-simple-xss-vulnerability/#sthash.DwtxUkUF.dpbs
https://kali.training/downloads/Kali-Linux-Revealed-1st-edition.pdf
https://www.exploit-db.com/
https://www.exploit-db.com/google-hacking-database



---
Please feel free to [contact me via email](mailto:mitchell.l.tuck@student.uts.edu.au) if you have any questions.

<!--more-->

---
