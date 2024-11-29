# LESSON 2: THREAT ACTORS  

### **BAD ACTOR / THREAT ACTOR:**  
- A person who attempts to steal, sabotage, or block access to computer systems or information.  
- Their targets are systems and data you are authorized to use, either stored or in transit between devices.  

They can have all different motivations. The motivations influence their attack method and provide insight into their character and beliefs. 

---

### **KEY CHARACTERISTICS OF BAD ACTORS**  
- **Motivations:** These can vary widely and influence attack methods.  
- **Groupings:** Can be classified based on their character, motivations, and common attack methods.  
- **Origins:** They can come from anywhere and be anyone.  

---

### **Examples of Bad Actors**  
1. **Local Coffee Shop Attacker**  
   - Sets up a fake Wi-Fi access point to steal user data.  
2. **Disgruntled Employee**  
   - Abuses their employee status to gain unauthorized access to corporate data.  
3. **Call Center Scammer**  
   - Operates from another country, scamming individuals as part of a full-time operation.  

---

### **TYPES OF BAD ACTORS:**  

#### **EXPLORER**  
- **Motivation:** Recognition and curiosity about system vulnerabilities.  
- **Methods:** Phishing (email), vishing (voice), smishing (text).  
- **Behavior:** Exploits weaknesses but does not intend serious damage.  
  - Example: Defacing a webpage to show their skills.  

#### **HACKTIVIST** 
Fervent believers in an external cause. They are motivated by ideology or are animated by an emotive force. The hacktivist's idealism causes them to act collectively in common cause against an enemy. While they may collectively crusade against a specific corporation, or go after political or social organizations that they feel did something bad, their extremism demands anonymity and online groups, by nature, are fragmented. 
- **Motivation:** Ideology or emotional force; crusades against corporations or political/social organizations.  
- **Methods:** DDoS attacks using botnets, targeting groups they view as adversaries because they don't have resources to make DDoS attacks on their own, they have to gain control of other people's computers.  
- **Behavior:** Operates anonymously; works in fragmented online groups.  

#### **CYBERTERRORIST**  
 Similar to hacktivist, their motivation is also driven by ideology. Cyberterrorists strive to intimidate and destabalize a society by destroying or destroying or disrupting computer or communication networks. They like to target online infrastructure like nuclear power plants, natural gas pipelines and electrical power grids. This type of online infrastructure is called operational technology. Unless sponsored by a nation state, they also lack the resources to inflict catastrophic destruction and must beg, borrow, or steal technology to mount effective attacks. Unlike hacktivists, they operate more like a cohesive virtual army. They have structure and direction. 
- **Motivation:** Driven by ideology to intimidate and destabilize societies.  
- **Methods:**  
  - Spear phishing campaigns: Identify someone with extensive network privileges, they target them with a carefully planned, social engineering campaign. 
  - Can use DDoS  
  - Attacks on operational technology (e.g., power grids, pipelines).  
- **Behavior:** Operates like a virtual army with structure and direction.  

#### **CYBERCRIMINAL**  
More self-centered: They want money plain and simple. They achieve this goal by a combination of phishing, theft of identities or credit cards, which they use or sell on the black market, or ransomware. 
- **Motivation:** Financial gain through phishing, identity theft, ransomware, and selling stolen data.  
- **Behavior:** Resourceful and profit-focused.  

#### **CYBERWARRIOR**  
 the least self-interested, but are nonetheless the most dangerous because they have the resources of a nation-state at their disposal. Cyberwarriors are motivated by the national interests of their home country. Whether cyberwarriors are good, bad or neutral depends on which nation-state they fight for. Their methods are vast and sometimes secret, and their missions include espionage, extortion, and embarrassment on the one hand, to using targeted cyberweapons to disrupt, damage, or destroy critical infrastructure on the other. They like to leverage unpatched vulnerabilities in common operating systems and applications, known as Zero Day Exploits. Cyberwarriors do intensive research on these common operating systems and applications, finding weaknesses, bugs, and other behaviors that they can use to attack the enemy’s computer systems. The weaknesses must remain a secret until they can be used because once they are known the vendor will issue a patch immediately.
- **Motivation:** Serves national interests of their home country.  
- **Methods:** Espionage, extortion, sabotage, zero-day exploits.  
- **Behavior:** Equipped with advanced resources; works on critical infrastructure or intelligence missions.  

---

Sometimes there can be multiple motivations for a group, or two or more bad actor types. For example, it would not be unusual for cybercriminals and cyberterrorists or cyberwarriors to collaborate on an attack or to exist within the same group. In the example of the 2021 cyberattack against Colonial Pipeline, the criminal organization’s host country is suspected to have abetted or approved of the attack. This is an example of cybercriminals and cyberwarriors colluding.

---


## **METHODS USED:**
### **PHISHING**  
- **Definition:** Social engineering attack tricking users into giving personal information.  
- **Types:**  
  - **PHISHING:** Generalized email-based attacks.  
  - **SPEAR PHISHING:** A social engineering attack using email with the intent of stealing confidential information or profiting in some other way and targeting a specific individual or group.   
  - **VISHING:** A form of phishing attack that takes place over voice over IP (VOIP). The bad actor often falsifies their caller ID to appear as if their call is coming from a legitimate source like a bank, law enforcement, charity.  
  - **SMISHING:** A form of phishing that uses text messages or SMS on mobile phones as the attack platform. The bad actor executes that attack with the intent to steal confidential information or profit in some other way.
 
- **Goals:**  
  1. Gain trust or appear legitimate.  
  2. Create urgency to force action.  

---

### **DDoS ATTACK (Distributed Denial of Service)**  
- **Definition:** Overwhelming a target server with traffic to make it unresponsive.  
- **Steps to Create a Botnet:**  
  1. Set up a Command & Control (C&C) server that is accessible on the internet. This is a central coordination point for all the botnet nodes.
  2. They craft malware that once installed, on some unsuspecting computers, waits patiently for instructions from the C&S server.
  3. Deploy malware to create botnet nodes.  
  4. The C&C server instructs hundreds of botnet nodes to send messages to the targeted server, which becomes overwhelmed by requests and stops responding. 

---

### **Ransomware**  
- **Definition:** Malware that blocks access to systems or data until a ransom is paid.  
- **Example:**  
  - **Colonial Pipeline Attack (2021):**  In 2021, a suspected Russian speaking criminal hacking group named DarkSide successfully breached the network of Colonial Pipelines which supplies gasoline and aviation fuel from texas to the us eastern seaboard. The criminal group stole 100 gigabytes of data and infected Colonial's network with malware that impacted the computerized equipment used to manage the pipeline. The pipeline was offline for nearly a week and the company was forced to pay 4.4 million to DarkSide to restore its system and recover its data. 

---

### **ZERO DAY EXPLOITS**  
- **Definition:** Leveraging unpatched vulnerabilities in systems.  
- **Example:** Attacking systems before vendors release patches.  

---

### **HACKER CATEGORIES**  
1. **WHITE HAT:** An ethical hacker who with proper authorization, probes the network to identify vulnerabilities 
2. **BLACK HAT:** Malicious hackers seeking profit or causing harm.  
3. **GREY HAT:** Operates outside legal boundaries but lacks malicious intent.  
4. **BLUE HAT:** Varient of white hat, security consultants performing penetration testing before system launches to detect and close vulnerabilities. 

---
***
---

### **KNOWLEDGE CHECK**  
- **Explorer:** Craves recognition.  
- **Cybercriminal:** Driven by money.  
- **Cyberterrorist:** Aims to intimidate a society.  
- **Hacktivist:** Motivated by ideology.  
- **Cyberwarrior:** Serves a national government.

---
***
---
