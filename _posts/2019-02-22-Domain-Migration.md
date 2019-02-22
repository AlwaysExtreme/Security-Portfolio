---
# title: "GitHub to Private Domain Migration"
tags: Cybersecurity, UTS, Summer-Studio, Cyber-Security-An-Offensive-Mindset, Domain-Migration
---
___
?????














# Conversion to Cloudflare DNS
Created Cloudflare account
Added Cloudflares two DNS to Domain account - 

## Security + Encryption features added:
Added **Clodflares DNSSEC** to Domain account - protects against forged DNS answers.
**SSL Full (strict)**: Your origin has a valid certificate (not expired and signed by a trusted CA or Cloudflare Origin CA) installed. Cloudflare will connect over HTTPS and verify the cert on each request.
**Always Use HTTPS** 
**Minimum TLS Version 1.1**: TLS 1.1 can help your domain become compliant with PCI DSS 3.2
**Opportunistic Encryption** allows browsers to benefit from the improved performance of HTTP/2 by letting them know that your site is available over an encrypted connection. Browsers will continue to show “http” in the address bar, not “https”.
**Onion Routing** allows routing traffic from legitimate users on the Tor network through Cloudflare’s onion services rather than exit nodes, thereby improving privacy of the users and enabling more fine-grained protection.
**TLS 1.3 Enable** TLS 1.3 is the newest, fastest, and most secure version of the TLS protocol. SSL/TLS is the protocol that encrypts communication between users and your website. When web traffic is encrypted with TLS, users will see the green padlock in their browser window. By turning on the TLS 1.3 feature, traffic to and from your website will be served over the TLS 1.3 protocol when supported by clients. 0-RTT is a feature that improves performance for clients who have previously connected to your website. It allows the client’s first request to be sent before the TLS connection is fully established, resulting in faster connection times.
**Automatic HTTPS Rewrites** Automatic HTTPS Rewrites helps fix mixed content by changing “http” to “https” for all resources or links on your web site that can be served with HTTPS.
**Security Level High**
Adjust your website’s Security Level to determine which visitors will receive a challenge page. Challenges all visitors that have exhibited threatening behavior within the last 14 days

IP Firewall:
**Unmetered DDoS Mitigation** Cloudflare will stand in front of your website regardless of attack size or duration.

WAF:
**Browser Integrity Check**, Evaluate HTTP headers from your visitors browser for threats. If a threat is found a block page will be delivered.

Scrape Shield:
**Email Address Obfuscation** Display obfuscated email addresses on your website to prevent harvesting by bots and spammers, without visible changes to the address for human visitors.
**Server-side Excludes** Automatically hide specific content from disreputable visitors.
**Hotlink Protection** Protect your images from off-site linking.




## Performance
**Auto Minify** HTML/Javascript/CSS, Reduce the file size of source code on your website.
**Brotli** Speed up page load times for your visitor’s HTTPS traffic by applying Brotli compression.
**Rocket Loader™** Improve the paint time for pages that include Javascript.
**Always Online™** If your server goes down, Cloudflare will serve your website’s static pages from our cache.

## Network
**QUIC** waitlist (Quick UDP Internet Connections) is a new encrypted-by-default Internet transport protocol, that provides a number of improvements designed to accelerate HTTP traffic as well as make it more secure
**IPv6 Compatibility** Enable IPv6 support and gateway.
**HTTP/2** Accelerate your website with HTTP/2
**IP Geolocation** mInclude the country code of the visitor location with all requests to your website. Note: You must retrieve the IP Geolocation information from the CF-IPCountry HTTP header.

## Applications
???
Contact Form added, Captchas enabled

---
Please feel free to [contact me via email](mailto:mitchell.l.tuck@student.uts.edu.au) if you have any questions.

<!--more-->

---
