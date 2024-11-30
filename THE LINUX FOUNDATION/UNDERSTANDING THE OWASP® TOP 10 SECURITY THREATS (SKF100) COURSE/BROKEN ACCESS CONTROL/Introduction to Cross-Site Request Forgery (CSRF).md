# INTRODUCTION TO CROSS SITE REQUEST FORGERY (CSRF)

CSRF is a web application vulnerability that allows an attacker to perform unauthorized actions on behalf of an unsuspecting user. The vulnerability arises from the trust web applications place in their users’ browsers.

## How CSRF Works

- The attacker tricks the user into performing actions on a site they are already authenticated on, without the user’s consent. These actions can include:
  - Changing account settings
  - Performing transactions
  - Deleting data
  
## Execution of CSRF

- The attack exploits the web application's failure to validate the source of incoming requests.
- Malicious links are crafted and embedded in emails or web pages.
- When the user clicks the link, their browser unknowingly sends the request to the web application, executing the unintended action.

- **FLOW OF THE CSRF ATTACK**
  ![image](https://github.com/user-attachments/assets/592cbde0-7e58-4e95-bef2-f4dea4f8000b)
