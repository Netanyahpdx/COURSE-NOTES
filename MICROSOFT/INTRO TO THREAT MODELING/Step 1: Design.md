# STEP 1: DESIGN #

The design phase is the starting ground for your threat modeling activities. 
Gather as much data as possible about what you're building and what you're using to build it.

GOALS
- Develop a clear picture of how your system works
- List every service consumed by your system
- Enumerate all the assumptions about the environment and default security configurations
- Create a data flow diagram that uses the right context depth level

Important: If you don't complete this phase, you might overlook important security design considerations for your system, which can put your customers at risk.

---

**ASK QUESTIONS ABOUT YOUR SYSTEM**
Ask as many questions as possible about your system. Here are a few questions to consider:

Area	                QUESTIONS
System description	  What does the system do? What are the business processes handled by the service? Are they clearly defined?  
System environment	  Will the system be built on the cloud or on premises? On which operating system is it built?   
                      Does it use containers? Is the system an application, service, or something entirely different?  
Scenarios	            How will the system be used? How will it not be used?   
Permissions          	Does the system have script execution, data, or hardware access requirements? If so, what are they?    
Cloud provider	      Which cloud provider does the system use? What default security configuration options does the provider offer?   
                      How do these options affect the system security requirements?   
Operating system	    Which Operating System will the system use? What default security configuration options does the operating   
                      system offer? How do these options affect the system security requirements?  
1st & 3rd PARTY 	    Which 1st & 3rd party services will the system use? What default security configuration options do they offer?  
                      How do these options affect the system security requirements?  
Accounts	            What are the account types that the system uses, like users and administrators? Are these accounts be   
                      local or cloud enabled? What access do they need and why?  
Identity &            How does the system help secure those accounts? Does it rely on Microsoft Entra ID? Does it use features   
access control        like Access Control Lists (ACL), multifactor authentication (MFA), and Session control?  
Tokens & sessions	    Will the system process requests like SOAP or REST APIs? How does it handle different sessions?  
Bypass	              Will the system use or require back doors? If so, how does that bypass work?  
Logging, monitoring   What are the mechanisms the system uses to log security events, monitor for anomalies, and back up  
                      system data? Which event types does capture?  
& backing up	
Network	              What are all the intrusion, detection, and protection systems that will be used? How is communication encrypted?  
Data	                What type of data will the system create or handle? What will the data classification type be? How does the   
                      system trust data sources? How does it parse data? What are the expected input and output behaviors? How is   
                      validation handled? How is data encrypted across all states?   
Secrets management	  How does the system handle keys, certificates, and credentials?   
  
Important: This list is extensive, but not exhaustive. Speak with your colleagues and security team to capture all relevant context for the system.   
Note: If you have a dedicated security team, schedule a whiteboarding session with them to go over the initial design. This contact can save you a considerable amount of time.

---

**CREATE A DATA FLOW DIAGRAM**
Use the answers to create a data flow diagram. Your diagram shows data across each stage in the data lifecycle, and includes changes in trust zones.   
Examples include:  
- Human users sign into your web application hosted in Azure to access data
- Administrators change default security configurations for elastic resources used by the web application
- Automated daily scripts monitor activity logs for the web application and notify administrators of any anomalies
Microsoft engineering teams submit data flow diagrams as part of their security compliance requirements. These diagrams make it easier to conduct security conversations.

---

**DIAGRAMING TOOLS**   
Microsoft engineers recommend using 1 of 2 tools available today:
- Threat Modeling Tool
 -Visio

---

**DIAGRAM ELEMENTS**
A data flow diagram shows the flow of data in a given system. It usually starts with requests from users or 
data stores and ends with data stores or Analytics Services. The data flow diagram uses distinct shapes to 
indicate the elements they represent.  
  
![image](https://github.com/user-attachments/assets/8eaace09-f62e-4a94-ae37-def74f670851)  

Data flow diagram elements also need context to help anyone understand how they're used and secured in the system.  
  
---
  
**INFORMATION TO INCLUDE IN THE DATA FLOW DIAGRAM**  
The amount of information to include in the data flow diagram depends on a few key factors:  
  
![image](https://github.com/user-attachments/assets/5b3a4b5a-6d7a-4a6e-a5e1-455d493850b1)  
  
Failure to include the right context leads to incomplete security reviews and potentially vulnerable systems.  
  
---
  
**DIAGRAM LAYERS**  
To help you understand how much information to include, choose between these 4 context depth layers:  
![image](https://github.com/user-attachments/assets/0d5181a2-4eab-4bdd-9d05-8cc233cd2e92)  
  
Note: Most data flow diagrams should contain both Layers 0 and 1 depth layers. Speak with your security team to confirm the required layer depth.  

---
---

**CHECK YOUR KNOWLEDGE**
1. What happens at the Design Phase? 
You know how the system works or will work. You can also identify security requirements, guarantees, or gaps inherited from cloud providers and integrated services
