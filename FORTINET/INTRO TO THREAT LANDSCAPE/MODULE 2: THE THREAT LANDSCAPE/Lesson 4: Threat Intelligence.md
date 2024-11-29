# LESSON 4: THREAT INTELLIGENCE #
---

**THREAT INTELLIGENCE:**
According to Gartner, threat intelligence is evidence-based knowledge, including:
*- Context*
*- Mechanisms*
*- Indicators*
*- Implications*
*- Actionable Advice*
About an existing or emerging menace or hazard to assets that can be used to inform decisions regarding the subject's response to that menace or hazard.

**THREAT INTELLIGENCE 3 REQUISITE CHARACTERISTICS:**  
**RELEVANT:** Must be relevant to your organization. 
  Ex: If you receive information that there is a new computer virus that exploits a vulnerability in macOS, but your organization doesn't use Apple, then this information isn't relevant. It would be relevant to an organization that uses Apple.  

**ACTIONABLE:**  The intelligence provides sufficient information for you to take steps to protect your organization. 
  Ex: If you learned that the bad actor group Dynamite Panda had just launched a new campaign of attacks against medical facilities, this alone does not provide you with enough information to act upon.
  
**CONTEXTUAL:** There is enough information to enable an intelligence analyst to assess the threat.
 Ex: The macOS vulnerability mentioned earlier is a good example. While a vulnerability in macOS could be a cause for concern, if your organization is properly managing and scanning its network assets, the security team should be able to quickly determine whether there are any macOS devices anywhere on the network. If none exist, then there is most likely no threat to the organization from the vulnerability. It is that additional context—knowledge network assets—that can turn information into threat intelligence. 
The Dynamite Panda story example can also support this point. The information that this bad actor group exclusively targets specific US verticals becomes threat intelligence because it helps you to assess the threat to your own organization. When viewed or considered on their own, many pieces of information do not amount to threat intelligence. However, when considered along with other, additional information, that initial piece of information can become threat intelligence.

---

## WHERE DO YOU FIND THREAT INTELLIGENCE? ##

**EXTERNAL:** Can come from a variety of sources and the information is often free. Some external sources of threat intelligence are government sites, such as the Department of Homeland Security, the FBI, and the National Institute of Standards and Technology (NIST) in the United States. These sites generally do not provide specific intelligence about individual malware, but they do offer useful advice about how to protect yourself from attacks, such as ransomware, and timely information about trending scams and attack methods.
**INTERNAL:** The information gathered by your organization’s own IT security team. More specifically, internal sources come in the form of server logs, network device logs, past incident reports, captured network traffic, penetration test results, and more. This raw data is organized and contextualized into inforrmation, and some of that information is relevant, actionable, and contextual, which makes it threat intelligence.

**PRIVATE:** SANS Institute, FortiGuard, Fortinet research and threat intelligence service. Some services are offered by subscription, but much of the threat intelligence found on the FortiGuard site is available for free. It describes how individual malware variants work and uses a severity rating system to rank the danger that these variants pose. Organizations can use this information to prioritize resources to counter the most dangerous threats.
**PUBLIC:**
**- (CVSS) COMMON VULNERABILITY SCORING SYSTEM:** Is a free and open industry standard used to assess computer system vulnerabilities. A CVSS assessment produces a numeric score to rate severity. The score, which rates the vulnerability from zero to ten—ten being the most severe—is computed using different sets of metrics. The metrics include factors, such as how exploitable the vulnerability is, how the vulnerability impacts  systems, and how effective mitigation efforts are against new exploits as the campaign progresses. For a more detailed description of these metrics, search for common vulnerability scoring system in nvd.nist.gov/vulnmetrics/cvss. CVSS is an example of open-source intelligence (OSINT). If you search the internet for OSINT, you will discover many other sources of free threat intelligence.
**- MITRE ATT&CK:** Freely shares a knowledge base of adversary tactics and techniques.

**VERTICALS:**
Ex: Banks in Brazil share their threat intelligence with each other. There are also other threat intelligence services and tools, including open-source intelligence, like Maltego and the MISP project.

---

## RECOGNIZED STANDARDS: ##
Help to share and describe cyberthreats in a language that's understood by the cyber intelligence community. One standard is called structured threat information expression
(STIX). Another is called trusted automated exchange of indicator information (TAXII).

**STIX**
A collaborative, community-driven effort to define and develop a structured language to represent cyberthreat information. It provides information about bad actors, incidents that have occurred, indicators of compromise (IoC), and the tactics and exploits used to carry out attacks. STIX also recommends actions to mitigate the incidents that it reports.

**TAXII**
An application protocol for exchanging cyber threat intelligence (CTI) over HTTPS. It defines a RESTful API and a set of requirements for TAXII clients and servers. By using standardized services, messages, and message exchanges, TAXII eliminates the need for customized point-to-point exchange implementations and facilitates the sharing of vital CTI. As the diagram shows, an organization that is a TAXII client can request information and publish new threat intelligence to a TAXII server, which then can be shared with other subscribers.

**RESTful API:** An application programming interface that conforms to the constraints of REST architecture.   
**REST** Representational State Transfer ,which is a software interface that two computer systems use to exchange information securely over the internet.  
**API:** Application Programming Interface. An API is a type of software interface that offers a service to other pieces of software. 
**API SPECIFICATION:** A document or standard that describes how to build or use such a connection.

---

## A PROCESS THAT YOU CAN FOLLOW TO CONVERT MASS DATA INTO PURPOSIVE THREAT INTELLIGENCE THAT CAN BE ACTED UPON: ##

**1. IDENTIFY THE PRIMARY THREATS TO YOUR NETWORK**
   That is, those threats that are the most vital to stop. Because there is an inexhaustible volume of cyberthreats, it is impossible to stop them all, and to attempt to do so would dangerously disperse and diminish cyber defenses.  
   Websites such as CVSS and FortiGuard will help you answer this question, because they provide intelligence about the most current threats with their severity ratings.  
   But relevant threats may also be determined by your organization’s vertical or business. 
     Ex: If you are protecting a hospital from cyberattacks, then ransomware is likely high on the list of attack methods employed by threat actors. On the other hand, if you are defending the Department of Defense, then attacks involving exfiltration are more likely.
**2. ASSEMBLE THREAT INFORMATION FROM YOUR INTERNAL AND EXTERNAL SOURCES.**
**3. PROCESS THIS INFORMATION:**
- This might involve focusing on information that is most relevant to the primary threats that you identified in the first step. Processing will also likely entail defining baselines of normalcy in network activities. The purpose of this is to help you recognize abnormal network activities. By separating the noise from the signal–eliminating the inconsequential data–you are better able to focus on and process the relevant information. 
**4. ANALYZE THE INFORMATION AND LOOK FOR INDICATORS OF COMPROMISE (IoC):**
**5. DISSEMINATE ANALYSIS AND ANY NEW INFORMATION:**
- Disseminate analysis, along with any new information to friends and partners. This effort is facilitated by STIC, and TAXII
**6. IMPLEMENT LESSONS LEARNED:**
- Does the information alter which threats you consider the most dangerous to your organization? Does it affect what information you are collecting, or how you are processing and analyzing the information?

---

**KNOWLEDGE CHECK:**
Sort the cyber threat intelligence steps in the correct order. 
1. Identify the most critical cyberthreats.
2. Collect threat information.
3. Process the information.
4. Analyze and look for indicators of compromise (IoC).
5. Disseminate the information.
6. Implement the lessons learned. 
