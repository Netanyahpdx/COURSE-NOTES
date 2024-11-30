  # LESSON 2: CIPHERS #

## WHAT ARE CIPHERS?   

![image](https://github.com/user-attachments/assets/906fa16a-e3b0-4440-843e-9f20c411615a)


A **CIPHER** is a secret or disguised way of writing a code.   

In the digital world of computers, **cryptographic algorithms** are used as **ciphers** along with **digital keys** to convert plain text to ciphertext and back again.     

**ENCRYPTION & DECRYPTION**: Converting plain text to ciphertext and back again.  

**ALGORITHMS**: Usually public information. An algorithm is a finite sequence of rigorous, well defined instructions, typically used to solve a class of specific problems or to perform a computation. A cipher algorithm is specifically to encrypt and decrypt information. 

**KEYS**: Usually secrets.  

*But not always.*  

Secrets must be safe guarded.  

---

## SUBSTITUTION CIPHER TYPE

![image](https://github.com/user-attachments/assets/1479bcd8-7e9e-48b8-af11-8c6628692f5a)

Ciphers have been used since before the computer age.  
The simplest type of cipher is the **substitution cipher**.  
Julius Caesar used the **SUBSTITUTION CIPHER** when encrypting messages.   
During the encryption process, the letters of a plain text message are replaced by other letters.   
Think of the Western 26 letter alphabet.   
If you shifted the letters by 3, the message "hail Caesar" would become "kdlo fdhvdu", which is the cipher text.  
In order for the recipient of the message to decrypt the ciphertext, they would need to know the number of lettershifts and shift in the opposite direction.   
Thus, when shifting 3 letters to the left, a "K" becomes an "H", a "D" becomes an "A", and so on.   
**SHARED KEY:** The number of letter shifts.  
**METHOD:** The cipher algorithm.   

---

## TRANSPOSITIONAL CIPHER TEXT ##  

The transposition cipher is about rearranging letters, and is more complicated than the substitution cipher.  
  
EXAMPLE OF TRANSPOSITION CIPHER:   
    RAIL FENCE: so named because its schema resembles a fence.  
      
There can be any number of rows, but in this example there are 3:
![image](https://github.com/user-attachments/assets/6347d2db-91d5-4542-9d21-4daa091a2b55)

The plain text message is written in a zigzag form, resembling a rail fence.   
When enciphering the plain text, the letters are taken row by row.  
The message "He had a bad day. What a day Dad had." would be enciphered to what you see on the screen.  
The receiver of the ciphertext would have to know the number of rows.   
This information is the **SHARED SECRET / KEY**.  
EXAMPLE WITH 4 ROWS:  

![image](https://github.com/user-attachments/assets/4ff177a1-266e-44d5-9c5d-c2da532e6ea6)

---

## 1 TIME PAD CIPHER TYPE ##  

![image](https://github.com/user-attachments/assets/60422cc3-856a-4498-b786-ea758d3cc9cb)
  
The next cipher type, named **THE ONE TIME PAD**, introduces randomness to the substitution method.  
Whereas the substitution cipher uses one shift letter value for the entire message, the key pad cipher uses a different value for each letter in the message.  
Imagine the sender has a 26 sided die and they roll this die for each letter of the message.   
If the message began as "Hi Bob" and the first five rolls were 10, 4, 3, 11, and 18, then the message would be converted to "RMEZT".  
This cipher type has a powerful feature.   
The randomness of the die ensures that there are no repetitive patterns, and that there is an equal chance of converting a plain text letter to any one of the 26 letters of the alphabet.  
The Caesar shift letter cipher has 26 possible combinations, which would not take too much effort to break using a brute force attack.    
However, if each letter had 26 possibilities, then a 5 letter message would be 26 multiplied by itself 5X.   
This amounts to almost 12m possible combinations.  
Without the help of a computer, this ciphertext is virtually impossible to break.  

---

## SOLVE A 1 TIME PAD CIPHER ##
![image](https://github.com/user-attachments/assets/d7c3d4f7-db23-4e19-902d-f629dd7344e1)

CIPHER TEXT: GDCHV  
KEY: 5, 21, 15, 1, 7  
Start at G, go 5 to the left = B  
Start at D, go 21 to the left = I  
Start at C, go 15 to the left = N  
Start at H, go 1 to the left = G  
Start at V, go 7 to the left = O  
TEXT = BINGO  

![image](https://github.com/user-attachments/assets/e4cfe055-b682-465a-b620-e3de4b393695)

---

## CIPHERS USED BY COMPUTERS ##

![image](https://github.com/user-attachments/assets/bf7da08a-fd90-4ceb-9d11-9451bd16e1eb)


2 cipher types that are commonly employed are:  

- **STREAM CIPHERS**:  
Encrypt a stream of plain text data, one bit / byte at a time. Stream ciphers are faster than block ciphers.  
    
Common stream ciphers that exist today are:  
    - **FISH**   
    - **RCS**  
     
- **BLOCK CIPHERS**:   
Block ciphers break the plain text into blocks for encryption.  
The size of the blocks is determined by the size of the key.  
If the key is 256 bits, then the blocks to be encrypted will also be 256 bits.    
If the size of the message is one megabyte, then the message would be divided into multiple blocks, each one 256 bits in size.    
    
Common block ciphers that exist today are:  
    - **(DES) DATA ENCRYPTION STANDARD**  
    - **3DES**  
    - **(AES) ADVANCED ENCRYPTION STANDARD**   
    - **Blowfish**   

---

**KNOWLEDGE CHECK:**  
WHICH 2 STATEMENTS ARE TRUE?  
- The block cipher chunks the data into blocks before encrypting them
- The stream cipher is faster than the block cipher
