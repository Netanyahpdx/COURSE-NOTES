# LESSON 5: PUBLIC KEY INFRASTRUCTURE #

## WHAT IS A PUBLIC KEY INFRASTRUCTURE?##

![image](https://github.com/user-attachments/assets/a25d8370-8e3a-4733-b8d7-8be29c944cb4)

(PKI) PUBLIC KEY INFRASTRUCTURE: An ecosystem comprised of the policies, procedures, software, and hardware needed to create, distribute, store, use, and revoke digital certificates.   
A certificate is revoked when it is no longer trusted.  
Consequently, the content in the revoked certificate, such as a public key, is rendered void.   
  
4 entities compose a PKI:     
- (CA) CERTIFICATION AUTHORITY
- (RA) REGISTRATION AUTHORITY
- DIRECTORY SERVER
- END ENTITY

---

## WHAT IS A DIGITAL CERTIFICATE? ##

DIGITAL CERTIFICATE: An electronic document, issued and signed by a trusted entity, such as a CA.
It contains the name of the certificate holder and may or may not contain a public key. 
If the certificate is issued to a specific person, device or application, it binds the entity's identity to the public key by way of a digital signature.
The certificate is trusted because it is signed by a trusted entity, just like a driver's license is trusted because it is issued by a government authority.
Although an encryption certificate contains a public encryption key used for encipherment, and a verification certificate contains a public verification key used for verifying a signature, not all certificates contain keys.
Policy certificates contain policy information, such as defining password criteria to secure your key store.
Certificate revocation lists (CRLs) are certificates that contain information about revoked certificates, in other words certificates that are no longer trusted.

---

There are different standards and best practices for the production and management of certificates, but perhaps the most important one is **X.509 version 3**.  
This standard defines what content can be written to a certificate and
how the content is expressed.  

**CERTIFICATES:** Elements that allow trust and secure communications between entities within a private or public domain.  
Given their importance, the certificate issuer—the CA—deserves critical consideration.   
  

**Common fields in a certificate are:** 
 
- **SERIAL NUMBER:** A unique value assigned by the trusted entity, or CA, that created the certificate. Because the certificate serial # is unique within the system, just like a driver's license is unique within a state, it can be used to identify the certificate. (EX: Revoked certificates are identified in CRLs by their serial #s)  
  
- **ALGORITHMS:** The algorithms identified in a certificate are those used to hash and sign the certificate - in other words, encrypt the hash result.   
  
- **VALIDITY PERIOD:** Defines the range of dates and times within which the certificate is valid. Any date or time that falls outside of the validity period represents time when the certificate is not valid and, just like an ID, an invalid or expired certificate cannot be used.   
    
- **ISSUER NAME:** Identifies the trusted entity that issued the certificate. A trusted entity is often a CA. The name is expressed as a distinguished name (DN). The DN maps to the entity's entry in a directory server. The entries are organized in a hierarchical fashion, resembling a tree, and is referred to as a directory information tree (DIT)   
   
- **SUBJECT NAME:** Identifies the entity (person, device, or application), which is bound to the other content in the certificate. The subject name can be expressed as a DN, email address, fully qualified domain name  (FQDN), or some other identifier that would be unique within the system in which the certificates operate. A subject name may be obfuscated to keep the identity private. For example, imagine a company that issues certificates to its customers but it doesn't want to share the identities of the customers with its competitors.  
  
- **KEY VALUE:** The alphaneumeric code embedded in the certificate.  
  
-**KEY USAGE:** Defines how the key can be used. If the key usage attribute value is keyEncipherment, then the key pair is used to encrypt and decrypt. If the key usage attribute value is digitalSignature, then the key pair is used to sign and verify signatures. CA certificates must have the keyCertSign attribute value in order for the CA's keys to sign and verify certificates.   
   
---

## THE CA & THE FOUNDATIONS OF TRUST ##

![image](https://github.com/user-attachments/assets/21d65c3f-a2ef-4d2b-8b52-3cb0e0f39e42)

The CA performs 2 primary functions related to certificates.  
1st, the CA issues certificates to end entities, such as persons and devices, and issues certificates to help manage end-entity certificates.  
Examples of management certificates are CRLs and policy certificates.  
2nd, the CA provides an ecosystem of trust whereby all entities within that system can safely interact with 1 another.   
Trust hinges on the CA's private key because all certificates issued by the CA are signed by its private key.  
  
But why do end entities trust the public key?  
There are a number of reasons why end entities trust the CA.  
1 might be that they have a relationship with the trusted entity, just like a bank client has a relationship with their bank or a citizen has a relationship with their
government.   
However, there is a legal framework that supports this trust.   
With respect to PKI, a high-assurance CA can prove in court that the CA's key pair was created in a manner consistent with the highest security standards.   
Low-assurance CAs generally do not have the same rigorous legal requirements and may not implement all the same security elements as a high-assurance CA.   
Ultimately, the required degree of trust determines the assurance level and the PKI implementation.  

---

## KNOWLEDGE CHECK ##
SELECT THE FOUR COMPONENTS THAT MAKE UP A PKI
- RA - REGISTRATION AUTHORITY
- DIRECTORY SERVER
- CA - CERTIFICATION AUTHORITY
- END ENTITY

---

## MULTIPLE CA ENVIRONMENTS & THE CHAIN OF TRUST ##

In a PKI implementation, multiple CAs can be organized in different ways.   
In a hierarchical environment, there would be 1 root CA and one or more subordinate CAs.  

![image](https://github.com/user-attachments/assets/acf08ecf-aa57-42a9-bb4f-21695472f6f3)

The root CA is the source of trust and the subordinate CAs issue certificates to end entities.   
A subordinate CA can have a subordinate CA and so on, creating a deeper hierarchy.   
Also, it is possible for a CA in one PKI to trust a CA in another PKI by cross certifying.  
This is a lateral structure because the trust relationship exists between two CAs of different PKIs.  
In the process of cross certifying, cross certificates are created that allow users of 1 PKI to trust the users of another PKI and the reverse.  
The crosscertification process can take place between a root or subordinate CA from 1 PKI and a root or subordinate CA from another PKI.  

![image](https://github.com/user-attachments/assets/5b66cfe7-1ff3-4790-ac9a-c24bd10f58ea)



If you were to build a hierarchy of CAs from ground up, you would start with the source of trust—the root CA.  
The root CA's certificate is signed by its own private key.  
In this scenario, 2 subordinate CAs are created below the root.  
During the initialization of those subordinate CAs, the public keys are sent to the root CA to be written to X.509 certificates and signed by the root CA's private key.  
You could install a subordinate CA below 1 of these subordinate CAs.  
You repeat the certificate request process, except this time, the superior subordinate CA signs the certificate.  

---

## MULTIPLE CA ENVIRONMENTS & THE CHAIN OF TRUST ##
Assume that the violet subordinate CA signed Mia's certificate and the blue subordinate CA signed Noah's certificate.  
Noah sends Mia an important legal document, which he signs.   
Can Mia trust and validate Noah's signature?  
Yes, because of the chain of trust.  
The chain of trust is a series of associated certificates, each 1 relying on the other for trust.  

![image](https://github.com/user-attachments/assets/cdd6b169-ed45-4f02-80bd-42e06220dd24)


The chain progressively leads to the root CA—the source of trust.  
Mia's application can use Noah's public key, found in his certificate, to verify the signature on the document.  
This verification can prove the integrity of the data and the authenticity of the signature.  
However, at this point, Mia does not trust Noah's certificate.  
Mia's application retrieves the certificate of the CA that issued Noah's certificate.   
The blue subordinate CA public key verifies the integrity and authenticity of Noah's certificate, but Mia still does not trust Noah's certificate or the subordinate CA's certificate.  
Mia's application retrieves the certificate of the CA that issued the blue subordinate CA certificate, which is the root CA.   
Because the root CA is the source of trust for Mia, she trusts the Noah's certificates, and the blue subordinate CA.  
This process of following the chain of trust to its source allows Mia to trust any valid certificate within this PKI.  

---

## STORING CERTIFICATES IN THE DIRECTORY SERVER ##
  
When Mia decided to verify the signature on the document, she needed Noah's certificate.  
How did she get Noah's certificate?   
  
There are 2 possibilities:  
1 Noah's application sent the certificate, along with the signed document.  
2 Mia's application retrieved the certificate from a server.   
PKI standards anticipated that end entities would retrieve certificates from an X.500 and Lightweight Directory Access Protocol (LDAP)-compliant directory server.  
The directory server not only stores user and device certificates, but all of the PKI certificates as well.  
These would include policy, CRLs, authority revocation lists (ARLs), cross certificates, and CA certificates.  

![image](https://github.com/user-attachments/assets/a0610564-3af6-4039-9554-b61d41efe660)

- X500: A series of standards for directory services developed by the International Telecommunication Union (ITU-T)
- (LDAP) LIGHTWEIGHT DIRECTORY ACCESS PROTOCOL: An open, vendor-neutral industry-standard application protocol for accessing and maintaining distributed directory information services over an IP network.
- (ARL) AUTHORITY REVOCATION LIST: A certificate that lists revoked CA certificates and revoked cross certificates. Contrastingly, a CRL list revoked end entity certificates.

---

## REQUESTING A CERTIFICATE FROM THE REGISTRATOIN AUTHORITY ##

![image](https://github.com/user-attachments/assets/f4486b20-6a68-462a-b61f-ab85aef3fcf1)

A registration authority (RA) is a function for certificate enrollment used in PKIs. 
The RA verifies and forwards certificate requests to the CA.
A person who requires certificates for themselves, for a device, or for an application, applies online or in person to an RA. 
An RA can be an automated application or it can be manned by a person authorized to use an RA
application.
An RA is similar to an automobile licensing bureau. 
It must identify applicants and ensure that they meet the requirements for a car license. 
Likewise, an RA is responsible for vetting requests to ensure only authorized and legitimate persons or other entities receive certificates. 
The RA registers approved requests with the CA, which generates and supplies a 1 time authorization code to the requester.
The degree of vetting applied to the requests may be determined by the level of trust declared by the CA. 
In a high-assurance CA, you may have to present yourself in person to the RA. 
But for other types of certificates, such as SSL certificates, you can register for and purchase them online.

---

## USING A CERTIFICATE AT THE ENDPOINT ##

![image](https://github.com/user-attachments/assets/3b3c8ec7-7009-4e00-970d-c8760178b823)


At the endpoint, the user needs a cryptographic application to generate key pairs, submit a certificate request to the CA, and conduct cryptographic operations.
A certificate service request (CSR) can be submitted manually or can be automated to some degree.
Some cryptographic capability can come built into computer operating systems, such as Microsoft cryptographic service provider (CSP).

---

To review, these are the components of a PKI that relate to the certificate lifecycle.
The CA creates, distributes, and revokes certificates.
The directory server stores certificates.
The RA vets and registers end entities for certificates.
And end entities generate keys, submit CSRs, validate certificates, and use keys and certificates to encrypt and decrypt, and to sign and verify signatures.
All of these entities carry out their functions in accordance with policy, which is prescribed by PKI authorities.

---

**KNOWLEDGE CHECK:**

![image](https://github.com/user-attachments/assets/261b33d9-7988-48f4-8257-e10b7791c1c7)
