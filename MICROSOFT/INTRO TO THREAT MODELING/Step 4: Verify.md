# STEP 4: VERIFY #
  
The verify phase is the last step of the threat modeling process, which often happens before the system is deployed. It involves ensuring requirements are met, assumptions are validated, and security controls are in place.  
  
---
  
**GOALS**  
  
- Confirm that the system satisfies all previous and new security requirements.  
- Configure cloud provider, operating system, and components to meet security requirements.  
- Ensure that all issues are addressed with the right security controls.  
- Take the system through manual and automated verification before deployment  
  
IMPORTANT: If you don't complete this phase, you won't be able to verify the security work was successfully completed.  
  
---
  
**VERIFY REQUIREMENTS & SET DEFAULTS**  
  
Start by verifying that all requirements created in the first phase are met.  
  
Examples:  
- Network security plans  
- Secrets management solution implementation  
- Logging and monitoring systems  
- Identity and access controls  
Then make sure to change all the default configuration settings from the cloud provider, operating system, and components so you can meet all security requirements.  
  
Examples:  
- Enable Azure SQL Database transparent data encryption to protect data on disk.  
- Use role-based access control to assign permissions to users, groups, and applications.  
- Enable Windows Firewall across all profiles.  
You should resolve all issues logged in the bug management solution. Verify all fixes.  
  
---
  
**RUN VERIFICATION**  
  
The last part involves running both manual and automated verification. At Microsoft, systems are subject to a verification process before deployment. The process might include automated scanners, code reviews, and penetration tests. The process can be enforced before each deployment or across time intervals, *like every 6-12 months*.  
  
If you answer *Yes* to any of the following questions, you might want to have shorter verification cadences:  
- Is my system used externally?  
- Does my system handle confidential data?  
- Do I have to comply with regulations?  
- Does my organization require extra security processes such as privacy implications, operational risk, or development requirements?  
  
---
  
**CHECK YOUR KNOWLEDGE**   
1. What happens at the Verify Phase?  
System is verified manually or automatically against previously generated threats to verify security controls reduced or eliminated risk.



