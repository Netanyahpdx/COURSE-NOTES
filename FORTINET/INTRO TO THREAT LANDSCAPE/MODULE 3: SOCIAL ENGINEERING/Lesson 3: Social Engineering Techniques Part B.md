# LESSON 3: SOCIAL ENGINEERING TECHINIQUES PART B #

Less intrusive

**SCAREWARE ATTACK:** Instilling fear through misinformation 
- Ex: A pop up window misinforms you that your computer is infected and directs you to download software that is either fake or malicioius. 

**WATERING HOLE:** Compromise a site that target frequents. 
- Ex: Red Sparrow, the movie. 
- Ex: An exiting location, either physical or online, is used for a chance encounter with the target. However, what appears to the target to be a chance encounter, is, in fact, a deliberate encounter that has been orchestrated by the bad actor.

**HONEYPOT TRAP:** Attracting the target with something enticing.
- Ex: Some secret services in other countries groom pretty educated women to act as professional temptresses. 
- Virtual trap to lure attackers, so white hat analysts can study their tactics to improve network security. An example is Forty deceptor by Fortinet. 
  
**TAILGATING:** Exploiting social conventions to gain access to a physical facility or access controlled room. 
-Ex: A fake UPS guy with his hands full of packages convinces someone with access to hold door open for him. 

---

## MULTI ATTACK METHOD APPROACH ##
 Worms, ransomware, trojan horse, backdoor, bot, zero day attacks are all tools in a toolbox that they can use when needed. 

---

## REAL LIFE EXAMPLE SOCIAL ENGINEERING BY BLUE HAT PEN TESTING TEAM ##
- Analyst reported the results at the RSA Europe Security Conference in 2012
- Revealed organization specializes in cybersecurity.
- Prepared for attack by building a credible online identity on Linked In for an attractive fictitious woman named Emily Williams.
- Also set up info about her on other websites, so people could match info on social media with google.
- Posted on university forums using her name
- 28 year old mit grad with 10 years experience, just hired by targetted organization.
- Within 15 hours, 60 FB friends and 55 linked in connections with targeted org. and contractors.
- within 24 hours, she had 3 job offers from other companies.
- Soon, she received LinkedIn endorsements for skills and men working for the targeted org. offered to help her get started faster in her new job.
- The men provided her with a work laptop and network access while skirting proper channels and normal procedures.
- She was granted more network privileges than she normally would have received as a new hire.
- The pen team didnt use the laptop or network access and continued with social engineering.
- Team created a site with a xmas card and posted a link to it on her social media profiles.
- People who visited this site, were prompted to execute a signed Java applet that opened a reverse shell back to the attack team, by way of an SSL connection.
- Once they had a shell, they used privileged escalation exploits to gain administrative rights
- They were then able to sniff passwords, install applications, and steal docs contatining sensitive information.
- Contractors for targeted org. were also deceived by the xmas card attack including employees by antivirus companies.
- one being a developer with access to source code. It might have been possible to compromise the source code that was being written for the targeted org.
- This would have made detecting the attack on the organization even more difficult. 
- Through FB, the pen team learned from 2 employees that the head of information security at their organization was about to celebrate his birthday
- That individual didn't have social media, but the pen team sent him an email with a birthday card that appeared to come from one of the 2 employees who had been talking about the event on FB.
- After he clicked the link in the malicious BDAY card, the computer became infected with malware.
- Because of elevated privileges within organization, much of network and sensitive information also became compromised.
- The Emily williams attack started by targeting low level employees like sales by befriending them first by gaining credibility and trust.
- This made it easier to befriend higher ups. Eventually moving on to security people and executives. 

  
**JAVA APPLETS:** Small applications written in the Java programming language. They are used to provide interactive features to web applications and can be executed by browsers for many platforms. Because they are small, portable programs embedded in HTML pages and can run automatically when the pages are viewed, they are excellent vehicles of attack by bad actors. 
**REVERSE SHELL / REMOTE SHELLS / CONNECT BACK SHELLS:** Take advantage of the target system's vulnerabilities to initiate a shell session and then access the victim's computer.

---

**KNOWLEDGE CHECK:**
1. In the Emily Williams example, which attack method was used to gain laptop and network privileges?
-Watering hole.
2. Which type of attack focuses on a site or social platform that the target is known to frequent?
- Watering hole
