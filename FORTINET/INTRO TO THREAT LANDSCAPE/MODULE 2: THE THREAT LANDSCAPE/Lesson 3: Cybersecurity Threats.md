# LESSON 3: CYBERSECURITY THREATS #

**CYBERSECURITY THREAT:**   
An action exploiting a vulnerability that results in harm to a network or computer system. Bad actors are the instigators of cybersecurity threats. They exploit different attack vectors to achieve their goals. 

---

**ATTACK VECTOR:**   
Method used by a bad actor to illegally access or inhibit a network, system or facility. 

- **3 COMPONENTS OF AN ATTACK VECTOR:**   
      1. Vulnerability.    
      2. Mechanism or object that exploits the vulnerability.    
      3. The pathway to the vulnerability.    
      
- **ATTACK VECTORS > THREATS**  

- **Attack vectors can be divided into:**
  - Electronic Social Engineering 
  - Physical Social Engineering
  - Technical Vulnerabilities (computer misconfiguration)

---

**METHOD:** 
How a vulnerability is exploited. 

---

**ATTACK PATH:**
Preparation of an attack campaign. 
The chain of events that occurs when attack vectors are exploited. 

---

EXAMPLES: 

  
**SCENARIO:** Diego receives an email from a colleague asking him to review an attached document. He saves the doc to his HD and opens it. Diego didnt know that the sender wasn't really his colleague. The document installed malware onto his computer.  
**VULNERABILITY** = user  
**MECHANISM** = malware & socially engineered message that convinced him to download the document  
**PATHWAY** = email  

**SCENARIO:** An authorized person is entering a server room which is a restricted zone. He notices a technician laden with boxes and computer equipment loitering outside. She explains that she needs to upgrade some equipment, but forgot her access pass. The authorized person doesn't recognize her, but since she sounds convincing, he wants to be helpful so he opens the door and she passes through. While in the server room, she discretely connects a USB device to one of the servers that installs malware.   
**VULNERABILITY** = The authorized person who let them in, and an unprotected server.  
**MECHANISM** = Malware and the situation used to convince the man to allow her access to the server room.   
**PATHWAY** = Door into server room and the USB device that released the malware.   
**ATTACK VECTORS** = Access to facility, access to server room  
Server infection was merely the 1st stage in a chain of events that may include reconnaissance and the exfiltration of data.   

---

**MAIN CYBERSECURITY THREAT CATEGORIES:**  
**SOCIAL ENGINEERING:** Act of using psychological manipulation into tricking people into taking some kind of action that is contrary to their best interest
EX: Disclosing confidential information 
      -Gain trust of victim.
      -Compelling them to act
**MALWARE (MALICIOUS SOFTWARE:** Software that is designed to disrupt, damage, or gain unauthorized access to a computer system.
**UNAUTHORIZED ACCES**
 - **TO PHYSICAL PLACES OR COMPUTER SYSTEMS:** Can be a bad actor following an authorized person through a door after they have swiped their badge. This is known as **TAILGATING**
 - **UNAUTHORIZED DIGITAL ACCESS:** A bad actor looking over someone's shoulder as they type their credentials. 
**SYSTEM DESIGN FAILURE:** A security flaw in a computer system or application that the bad actor exploits to gain access to a computer system. 

---

** COMMON CYBERSECURITY ATTACK VECTORS:**
Attack vectors can be categorized in several ways and are often combined with other vectors to achieve the desired result.
EX: A distributed denial-of-service (DDoS) attack involves a command and control (C&C) server signaling to thousands of infected computers to send requests to a targeted server at the same time. However, before a DDoS attack can be invoked, the bad actor must first infect thousands of computers. How do they do that? One common method is **phishing**. The bad actor can send a **phishing email** to millions of unsuspecting users, and some of those users will click on the link provided that will install malware on their computers.

**NOT DDOS BOTNET, BUT USED FOR TROJAN MALWARE OR RANSOMWARE:**
**WHALE PHISHING:** a phishing attack aimed at a high-value target, such as a CEO or CFO of an organization. These individuals are targets because they have access privileges to servers and databases, which the bad actor wants access to. The email is carefully crafted to be plausible and personalized to ensure the target is not alerted to the scam. Within the email could be an attached document or a link. Once opened, the document appears entirely harmless, but behind the scenes malware is installed on the target’s computer. This is known as a **Trojan horse attack**. From there, the malware can leverage the individual’s network privileges to access and infect other computers. The initial targeted computer is merely the access point to the network in a multi-staged attack.
**SPEARPHISHING:** This type of phishing attack is focused on a specific individual or group of individuals. Unlike a regular phishing attack which is agnostic and doesn't distinguish between targets.   
**RANSOMWARE:** Ransomware is a type of malware that denies the user access to a system of information, often through encryption. 
**DoS & DDoS ATTACKS:** The main difference between a DoS and a DDoS is one of scale. DDoS has infected many more computers which the bad actor controls by way of the C&C server. 


Attack vectors can be used during both stages:
-To exploit a weakness to gain a foothold in a computer system.
-During the post exploit stage.  
  
The exploited weakness can be human, computer technology, or a combination of the two. 

**PHISHING** = HUMAN NATURE. (It is a default trait of human nature to trust, especially if a request seemingly comes from an official source or if you know the person or thing who is making the request.)

**BIRTHDAY ATTACK:**  PRE-EXPLOIT, 
This attack exploits a weakness in some hashing alorithms, which are often used to protect passwords. The weakness is that multiple input values produce the same output value. 

**BRUTE FORCE ATTACK:** PRE-EXPLOIT, Relies on human fallibility.  
A method used to try to steal someone's credentials. It involves simply trying every possible combinaion until the bad actor guesses correctly, but success relies on the targeted individual using a weak password.  
Neurtalize by enforcing a strong password policy. 

---

**KNOWLEDGE CHECK:**
1. Which three attack vectors are typically used during the pre-exploit stage of a cyberattack?
- Whale phishing
- Spearphishing
- Phishing
2. Which three components compose an attack vector?
- Vulnerability
- Mechanism
- Pathway



