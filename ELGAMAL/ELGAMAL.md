# ElGamal Encryption Algorithm

* public key cryptosystem
* invented by **Taher Elgamal** in 1985
* asymmetric key algorithm
* difficult is the discrete logarithm problem
* based on the Diffie-Hellman key exchange
* If we know $g^a$ and $g^b$, it is difficult to find $g^{ab}$.

## Components of ElGamal Encryption Algorithm

### **1** _ Key Generation (Public and Private Key)

    - select a large prime number p =17

    - select a primitive root of p, g=6

    - choose a random integer number  a=5 as  "private key"  1 < a < p-1

    - calculate e: e = g^a mod p :==> 6^5 mod 17 = 7

    - and  "public key"  is (p, g, e) = (17, 6, 7)

### **2** _ Encryption

    -first, you shuld have message M to encrypt M<p ( M=13 < 17 )

    -select a random integer number k=10 as "session key" 1 < k < p-1

    -C1 = g^k mod p :==> 6^10 mod 17 = 15

    -C2 = M*e^k mod p :==> 13* 7^10 mod 17 = 9

    -cipher text is (C1, C2) = (15, 9)

### **3** _ Decryption

    -x = C1^a mod p :==> 15^5 mod 17 = 2

    -M = C2*x^-1 mod p :==> 9*2^-1 mod 17 = 13

## Idea of ElGamal Cryptosystem

### it work with public key cryptosystem

    - you have a public key and a private key.

    - the public key is published for everyone to see.

    - the private key is kept secret.

    - any one that wants to send you a message can use your public to encrypt the message.
    
    - only you can decrypt the message using your private key.

## Applications

### 1 - Secure communication

### 2 - Digital signatures

### 3 - Secure electronic voting

## Advantages

### 1 - It is secure

### 2 - key distribution is easy

### 3 - digital signatures

## Disadvantages

### 1 - slow processing

### 2 - large key size
