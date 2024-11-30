# LESSON 4: HASHING & DIGITAL SIGNATURES #

## WHAT IS HASHING? ##

![image](https://github.com/user-attachments/assets/5671e912-0506-41d4-802f-9d54de6222f9)

HASHING: The process of converting data of an arbtrary size to a unique value of a fixed size.  
  
1. OUTPUT VALUE *(A hashing output value is also known as a hash value, hash codes, hash result, digests, or hashes. Cryptographers use the terms pre-image to refer to the input data, and image, to reference the hashing output value)*: Is a fixed length  
   - Determined by the hashing algorithm.  
   - Denies the bad actor information about the nature of the input data.  
  
2. OUTPUT VALUE IS UNIQUE FOR EVERY INPUT VALUE:  
   - Detects changes to input data when output value is different.  
   - Denies the bad actor the ability to alter data and get away with it.  
   - Avoids **collisions** *(Although rare, it's possible for a hashing algorithm to produce the same hash output for 2 distinct input values. This is known as a hash colllision. The probability of a hash collision, depends on the algorithm's output size. There are different strategies to avoid or reduce the chances of a collision. The simplest and most obvious is to use an algorithm with a larger sized output value.)*

3. HASHING *(Aside from cryptography, there are other uses for hashing, such as producing seemingly random strings, protecting passwords, and indexing data. In the last case, database engines use hashing to generate hash tables. Hash tables are hash output records of the information stored in the database. Using hash tables can help you speed up the process of finding the information that you are looking for)* IS NON-REVERSIBLE AND ONE WAY

---

## PRODUCE A DIGITAL SIGNATURE - SIGNING PROCESS ##
  
Combining the security features of hashing with asymmetric cryptography can produce a digital signature.  
A digital signature serves a number of purposes.   

![image](https://github.com/user-attachments/assets/179716c6-7e44-4c65-9c0c-33133cb8ba9b)
  
**DIGITAL SIGNATURES:**  
- Ensure the data integrity of the information signed.  
- Authenticate the person or thing that signed the information.  
- Support non repudiation *(The assurance that someone cannot deny the validity of something. B/c you have proof of the origin and integrity of the data, it's very difficult to dispute the identity of the signer and their association with and validity of the signed information.)*.   
  
**DIGITAL SIGNING PROCESS:**  
1st STEP: The information that needs to be signed is hashed. This produces an **output hash value**.  
2nd STEP: The asymmetric private signing key associated with the signer encrypts the output value using an asymmetric algorithm. This encrypted output value is called a **digital signature**.  
3rd STEP: The digital signature is attached to the information. In order to verify the signed information, you require the corresponding public verification key.  

---

## PRODUCE A DIGITAL SIGNATURE - VERIFYING PROCESS ##  

![image](https://github.com/user-attachments/assets/daa10d1d-fbec-4eed-9b53-2cb81296cf17)
  
In asymmetric cryptography, public keys are written to certificates.  
Certificates are issued and signed by a certificate authority (CA).  
In addition to the public key, the certificate bears the owner's name.  
The verification certificate can be retrieved from a repository by the receiver, or it can be attached to the signed document.  

**VERIFICATION PROCESS:**  

![image](https://github.com/user-attachments/assets/28bd577a-c627-4c1d-bab0-35e1055e28ba)

1st STEP:  
The receiver's application hashes the information, producing a new output value.  
2nd STEP:  
After verifying that the signer's verification certificate is valid, the public key decrypts (in other
words, verifies) the digital signature.  
3rd STEP:  
The verifier compares the new output value to the original output value.  
If they are the same, then you know that the information has not changed.  
Because the public key successfully decrypted the digital signature, and because the name of the owner of that key is written in the certificate, you can confirm the authenticity of the signer.  

---

## HASHING FUNCTIONS ##

There are a number of popular hash functions used in cryptographic operations.  

**COMMON HASH FUNCTIONS:**  
- (MD5) MESSAGE DIGEST 5 & MD6
- Secure hashing algorithm one (SHA-1), SHA-2, & SHA-3
    - SHA-2 includes SHA-224, SHA-256, SHA-384, & SHA-512
    - SHA-3 various output lengths
- Microsoft LANMAN and (NTLM)NT LAN Manager algorithm
- HAVEL & RIPEMD

---

## COMMON ATTACK METHODS: ##

**BRUTE FORCE ATTACK:** This means that the bad actor will try different input values until they produce the same value as the original hash output. 
  
  
A brute force attack is more effective if the bad actor has clues about the nature of the input data. 
If the attacker has no idea of the size of the input data, a brute force attack will have limited success.

![image](https://github.com/user-attachments/assets/6808e721-c03e-4ca9-b11e-40928de9fa6d)

However, if the attacker knows something about the input value, they can eliminate those input values that don't apply.  
EXAMPLES:  
If the input value is a password and the bad actor knows the password requirements (ex: that the minimum length is 10 characters, the maximum length is 20 characters, it must contain uppercase letters, lowercase letters, and numbers, but no special characters) then they can drastically narrow down the scope of their attack.  
  
If the bad actor knew that the hash output was protecting a 4 number PIN using MD5, then they could try every conceivable combination until they arrived at the same hash output.   
   
A type of **brute force attack** is the **BIRTHDAY ATTACK** *(which is based on the birthday paradox and exploits hashing functions that are known to produce collisions.)*   
If you were in a room with 183 people, there is a 50% chance that one of them shares your birthday.  
However, if you wanted to have a 50% chance of any 2 people sharing the same birthday, you would only need 23 people.  
This is the birthday paradox.   
    
For hashing functions, this means that it is much easier to find any 2 matches, if you don't care which 2 they
are.  
When attempting to crack a hashed password, the bad actor doesn't care if their input data matches the password,
only that their input data produces the same hash output.  
This is because servers don't store user passwords.   
They store the hashes of those passwords.  
So, if the bad actor can reproduce the hash output protecting Alice's password, they can log in as Alice.  
As noted earlier, a situation in which two or more input values produce the same output value is called a **collision**.  


The **birthday attack** exploits the mathematics behind the birthday problem in probability theory.   
The success of the **birthday attack** largely depends upon the higher likelihood of collisions being found between random attack attempts and a fixed degree of permutations.  
The best defense against a **brute force attack** is to ensure that the hash function supports an output that is long
enough to be computationally infeasible to break.  
When hashing is used to protect passwords, increasing the length of the hash output value may not be enough, if
the function is susceptible to collisions.  
In order to protect the password hashes stored on computers, you can increase entropy through the process of
**key stretching**.  


Click the underlined terms for more information.

**BIRTHDAY PARADOX:**  
To understand the math of the birthday paradox, it may be easier to calculate the odds that no one shares a
birthday and invert the results.  
Imagine that, as people enter a room, you ask them their birthdays.   
What is the chance that 2 people in that room share the same birthday?  
If 1 person enters the room, there is no chance that they share a birthday with anyone, because there is no 1
else in the room.   
However, after a 2nd person enters the room, there is 1 chance out of 365 that the 2 people now in the room share the same birthday.   
365 is the denominator, because there are 365 days in a year (omitting the leap year) or 365 possibilities.  
In other words, there is a 364/365 chance that these 2 people will not share the same birthday.  
When the 3rd person enters the room, they must avoid 2 birthdays.  
Thus, the chance that the 3rd person will not share a birthday with the 1st or 2nd person is 363/365.  
To determine the probability that none of the 3 people in the room share a birthday, you must multiply the last result with this fraction [0.9973 x 363/365].  
When the 4th person enters the room, they must avoid 3 birthdays.  
The last result, 0.9918, is multiplied by 362/365.  
If you advance ahead to the 23rd person entering the room, there are 23 days that you have to avoid;  
Therefore, a 343/365 chance of not sharing the same birthday.  
However, when you account for all the people in the room [0.5243 x 343/365], the result is a surprising 0.4927.  
In other words, there is about a 49% chance that 2 people in a room of 23 people will not share the same birthday, or a 51% chance that they will.  

![image](https://github.com/user-attachments/assets/c18ff402-f833-439b-999f-1c2c6e036b88)

**DEFENDING AGAINST BRUTE FORCE ATTACKS:**
- Increase the size of the hash output length
- Key Stretching *(In cryptography, key stretching is a technique used to make a weak key, such as a password, more secure by adding resources. The resources could be a combination of adding a random value (called a salt) to the key and hashing the combined values.)*

---

**KNOWLEDGE CHECK:**
WHICH 2 STATEMENTS ABOUT HASH FUNCTIONS ARE TRUE:
- A characteristic of a hash function is that it's non-reversible.
- A hash output is a fixed length. 
