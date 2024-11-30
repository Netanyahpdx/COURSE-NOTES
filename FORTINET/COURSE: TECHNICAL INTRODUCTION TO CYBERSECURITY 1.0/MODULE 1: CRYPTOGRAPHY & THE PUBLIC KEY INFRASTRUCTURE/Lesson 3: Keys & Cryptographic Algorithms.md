# LESSON 3: KEYS & CRYPTOGRAPHIC ALGORITHMS #

**DIGITAL KEY**: With respect to encryption, keys can be used to encipher the flow of information between two devices, bulk stationary data, or a small piece of data, such as another digital key or a hash output value.  
![image](https://github.com/user-attachments/assets/09be2946-84f4-4b6a-8fae-9951208c4b32)

Depending on the task that the key is performing, its lifetime could be years or a few seconds.  
EX:  
A key used to sign certificates might be valid for 10 or more years, but a key used to encrypt a session between two devices is only used for the duration of that session.   
Keys are usually kept private or secret, but they also can be public.  
Public keys are often written to digital certificates.  

**(MAC) MESSAGE AUTHENTICATION CODE:** A hash function that uses a digital key to ensure the integrity and authenticity of the message. 

---
---

## KEY LENGTHS AND STRENGTHS ##

PUBLIC KEYS are often 1024 bits, 2048 bits, or larger. Because of their relatively large size, public keys are often used to encrypt small pieces of data, like another key or a hash of data. To encrypt large amounts of data would take too long.    

![image](https://github.com/user-attachments/assets/1c4c3e82-6394-44a9-b918-56433fe98ccf)


Smaller keys, in the 128-bit to 256-bit range, are used to encrypt bulk data.   
So, the type or size of the key that is used is determined by the type of cryptographic operation being performed.  
- If you are encrypting a key to safely transfer it to another entity, then use a larger key.  
- If you are encrypting a stream of data where performance is critical, use a smaller key.  
  
While this rule of thumb is applied for performance reasons, there are also security issues to consider:  
- The length of the key impacts its strength, but length is not the only factor to consider when calculating key strength.  
- The complexity of the key is also an important factor.  
- Consider a password that is 10 characters long, but all 10 characters are digits. A 10 digit password has 10B possible permutations.  
- In contrast, an 8 character password that combines digits plus upper and lower letters has over 218T permutations.   
- Although 2 characters less in length, the latter password is much stronger than the former.  

---

## KEY STRETCHING ##

![image](https://github.com/user-attachments/assets/ac01a9dd-8fc6-4dba-8658-66497c616b15)

- Key stretching is a method used to strengthen keys or passwords that are either too short or predictable.  
- The process involves feeding the key or password into a hashing algorithm to produce an enhanced key or password.   
- Examples of stretching algorithms are password based key derivation function two (PBKDF2) and BCRYPT1.  
- BCRYPT is the default algorithm used for key stretching in OpenBSD and various Linux distributions.  
- When BCRYPT is used, a key or password is hashed multiple times before a 128-bit salt is added.  
- Then, the combined value is hashed once more.  
-The final hash output is the enhanced key or password.  
- **SALT** is a random value added that is added to another value to increase entropy.   

---

**KNOWLEDGE CHECK**  
LONGER KEY SIZES SUCH AS 2048 BITS ARE GENERALLY USED TO ENCRYPT SMALL BITS OF DATA SUCH AS HASH OUTPUTS.
- TRUE

---

## WHAT IS A SYMMETRIC ALGORITHM? ##

**SYMMETRIC ALGORITHM:**  
A cipher used to encrypt and decrypt data using the same key.  
With the exception of RC4, which is a stream cipher, the rest are block ciphers.  

![image](https://github.com/user-attachments/assets/899d003b-b354-4aae-9879-23c224ce965f)
   
- **(DES) DATA ENCRYPTION STANDARD:**   
DES is a symmetric key cipher developed by IBM and adopted by NIST in the 1970s. DES uses a 48 bit key to encrypt 64 bit blocks of data.    
  
- **3DES:**  
Triple DES is the DES cipher used to encrypt the plaintext data 3x.  
  
- **(IDEA) INTERNATIONAL DATA ENCRYPTION ALGORITHM:**  
AES is a 128 bit block symmetric key cipher using a 128, 192, or 256 bit key.  
Originally named the Rijndael algorithm after its 2 Belgian inventors, it was renamed AES when adopted by NIST as an encryption standard in 2001.    
   
- **(RC4, RC5, RC6) RIVEST CIPHER:**  
RC4, RC5, RC6 are symmetric key ciphers developed by Ron Rivest (RC6 was co-invented), although RC4 uses a different method than RC5 and RC6.  
      - RC4 is a stream cipher that uses 40 bit to 2048 bit keys.  
      - RC5 is a block cipher developed in 1994. The block and key sizes are configurable.  
      - RC6 is a 128 bit block cipher, derived from RC5, which was designed to meet the requirements of the AES algorithm competition.  
  The Rijndael cipher won this competition.   
  
- **BLOWFISH / TWOFISH:**  
Blowfish is a 64 bit block symmetric key cipher with variable length key sizes, released in 1993.  
TWOFISH is a 128 bit block symmetric key cipher, supporting 128, 192, and 256 bit key sizes, and was published in 1998. Like RC6, it was a contender in the AES algorithm competition. 
It is, in part, derived from BLOWFISH.
  
---

## SYMMETRIC KEY CRYPTOGRAPHY ##

![image](https://github.com/user-attachments/assets/cc7ac6b5-1c55-42bc-a785-d1f6eb21ab86)


The main advantage of symmetric cryptography is that it can encrypt and decrypt data more quickly than asymmetric cryptography.    
This is because symmetric keys are shorter than asymmetric keys, and symmetric cryptography uses the same key to encrypt and decrypt.   
Symmetric cryptography works in a way that is similar to a combination lock.   
Imagine that Frank, Javier, and Nora all work at the same facility and all need a key to access a secure room.  
They work different shifts, and the employer does not allow the key to leave the building.  
The employer secures the key in a lock box with a combination code.  
Frank, Joe, and Nora all need the combination code to access the key and to secure the key.  
However, this similarity to a combination lock exposes one disadvantage of symmetric cryptography.  Because you use the same key to encrypt the plaintext as you use to decrypt the cyphertext, the key must remain a secret to protect the data.  
How do you protect the secret key?   
If Alice encrypted a message for Bob, she could safely send the ciphertext, but how would she securely deliver the key?  

---

## HOW DOES SYMMETRIC CRYPTOGRAPHY WORK? ##

![image](https://github.com/user-attachments/assets/17619eaa-e6dd-4c2a-9d51-911485cbecb1)

To encrypt information using symmetric cryptography, a crypto application uses a symmetric key and cipher to convert the plaintext into ciphertext.  
In order to decrypt the ciphertext, the same symmetric key and cipher convert the ciphertext to plaintext.  
But the problem remains — how do you securely send the key to the receiving party?  

---

## WHAT IS AN ASYMMETRIC ALGORITHM? ##

An asymmetric algorithm is a cipher used for cryptographic operations using a pair of mathematically related keys.  
They can do all, or some, of these operations:  
A key exchange operation enables 2 parties to safely exchange a secret, or key, over a public channel, such as the internet.  
Asymmetric algorithms and cryptography are also known as public key algorithms and cryptography.  
Examples of asymmetric algorithms are:
  
- **DIFFIE-HELLMAN:**  
A key exchange protocol that enables 2 parties to safely exchange a secret or key. The concept of this key exchange method was conceived by Ralph Merkle. The algorithm was published in 1976 by Whitfield Diffie & Martin Hellman.
    
- **(RSA) RIVEST, SHAMIR, AND ADLEMAN:**  
A cipher that can encrypt, decrypt, sign and verify.
    
- **(ECC) ELLIPTIC CURVE CRYPTOGRAPHY:**  
ECC is an approach to asymmetric cryptography based on the algabraic structure of elliptic curves over finite fields. ECC uses smaller keys than other forms of cryptography.
    
- **(PGP) AND GPG PRETTY GOOD PRIVACY:**  
PGP is a cipher used for encryption and digital signature purposes. Developed by Paul Zimmerman in 1991, it is a popular email encryption tool. GPG is the open source version of PGP
    
- **(DSA) DIGITAL SIGNING ALGORITHM:**  
DSA is a cipher used for digital signature operations and is a Federal Information Processing Standard. In 1994, NIST adopted DSA as its digital signature standard (DSS) as FIPS 186. 
  
---

## ASYMMETRIC KEY CRYPTOGRAPHY ##

![image](https://github.com/user-attachments/assets/b931d20e-8dec-43fa-b6a5-71e0fab53e13)

Increased data security is the primary benefit of asymmetric cryptography.  
This is because users are never required to share their private keys.  
Asymmetric cryptography employs a pair of mathematically related keys.  
For encryption, the public key encrypts and the private key decrypts.  
Asymmetric cryptography is similar to a lock and key.  
The lock secures the item and only the correct key can unlock the lock.  
The principal disadvantage of asymmetric cryptography is that the crypto processes are very slow compared to
symmetric cryptography.  
This becomes a problem when you are streaming encrypted data between two points, or when you need to encrypt and decrypt large amounts of data.  
The slowness of asymmetric cryptography does not make it viable in these circumstances.   

---

## HOW DOES ASYMMETRIC CRYPTOGRAPHY WORK?##

![image](https://github.com/user-attachments/assets/1c2c0eff-06b6-44c3-adc7-2f0215012e27)

During the encryption process, the sender's crypto application converts the plaintext data to ciphertext using the recipient's asymmetric public key and an asymmetric cipher.  
During the decryption process, the recipient's crypto application converts the ciphertext to plaintext using their private decryption key and the same asymmetric cipher that the sender used.  

---

## COMBINING SYMMETRIC & ASYMMETRIC CRYPTOGRAPHY ##
  
![image](https://github.com/user-attachments/assets/a1fccd47-5c34-442a-9e4a-1409293dedc1)  
  
The main disadvantage of symmetric encryption is securely delivering the key to the recipient, while the main disadvantage of asymmetric encryption is its slowness.  
When symmetric and asymmetric cryptography are combined, the disadvantages of both are remedied.  
Symmetric encryption secures bulk data to ensure good performance, while the symmetric key a small piece of data is encrypted by the recipient's public asymmetric key.  
Thus, the question "How do we securely send the key to the receiving party?" is answered.  
In a scenario where the processes are combined, Alice sends an encrypted message to Bob.  

---

**STEPS OF ENCRYPTION:**  
1ST STEP: Alice's crypto application generates a 1 time symmetric key and, together with a symmetric algorithm, encrypts the message.  
  
![image](https://github.com/user-attachments/assets/329f9601-3e73-47d5-994e-ba8cf62bcfae)  
  
STEP 2: The application retrieves Bob's public encryption key and uses this key, together with an
asymmetric algorithm, to encrypt the symmetric key.  
  
![image](https://github.com/user-attachments/assets/e556ba45-251d-4853-a455-7e03fb646a98)  
  
STEP 3: The encrypted message and key are sent to Bob.  

---

**STEPS OF DECRYPTION:**  
STEP 4: Bob's crypto application retrieves the private key from his secure key store. At this stage, Bob may be required to submit credentials. The private decryption key, together with the same asymmetric algorithm that Alice used, decrypts the symmetric key.  
  
![image](https://github.com/user-attachments/assets/69ad2a94-b962-4745-923a-bfaf3e81efd1)  
  
  
STEP 5: The symmetric key, together with the same symmetric algorithm that Alice used, are used to
decrypt the bulk data.

---

**KNOWLEDGE CHECK:**
IN A SCENARIO, WHERE BOTH ASYMMETRI AND SYMMETRIC CRYPTOGRAPHY ARE USED TO ENCRYPT A MESSAGE, WHICH KEY IS USED TO ENCRYPT THE SECRET SYMMETRIC KEY?  
- The receiver's public key

