# DM 103347 : RSA Cryptography #
### PROJECT MEMBERS ###
StdID | Name
------------ | -------------
**63910** | **Muhammad Ashar** 
63866 | Mohammad Dursham
63924 | Misbah Shakeel
62606 | Muhammad Azhar
63927 | Abdullah Afaque
## Project Description ##
This is RSA Cryptograpy simulation, RSA is an asymmetric cryptography meaning it works on 2 keys which are public and private keys both keys are derived from the same 2 user input prime numbers the strength lies in the length/size of key since it is hard to factorize large numbers, we aimed to give the user complete input control.

## Discrete Math Concepts Used ##
we have used GCD,Modular Multiplicative Inverse,printing of relatively prime numbers and Euler's Function, firstly GCD is used to find the relatively prime numbers in the method of coprime in the code, secondly Modular Multiplicative Inverse is used for encryption and decryption in encrypt_block and decrypt_block method respectively and it is also used for deriving private key, coprime method is used to print the list relativly prime number where each number is greater than 1 and less than the euler's function this list is printed for the selection of 'e', lastly euler's function is used for the printing of relatively prime numbers and derving of private key

### Example 1: GCD ###
Method of GCD. 
```Python
def gcd(a, b):
    while b != 0:
        c = a % b
        a = b
        b = c
    return a
```
### Example 2: List of Relatively Prime Numbers ###
Method of coprime. 
```Python
def coprimes(a):
    l = []
    for x in range(2, a):
        if gcd(a, x) == 1 and modinv(x,phi) != None:
            l.append(x)
    for x in l:
        if x == modinv(x,phi):
            l.remove(x)
    return l
```
### Example 3: Modular Multiplicative Inverse ###
Method of modinv. 
```Python
def modinv(a, m):
    for x in range(1, m):
        if (a * x) % m == 1:
            return x
    return None
```
### Example 4: Euler's Function ###
Code of Euler's Function. 
```Python
phi=(p-1)*(q-1)
print("Euler's function [phi(n)]:" + str(phi) + "\n")
```

## Problems Faced ##
The problems we faced were that at times the code didn't print decrypted or encrypted value and second was faced at the start of project which was to return the encrypt or decrypt block as a string.

### Problem 1: not printing  encrpyted and decrypted data ###
we resolved this issue by structuring the data in different method sice in python methods can be created in middle of code because of that at times some values of variable would change causing hindrance in either printing encrypted or decrypted data. 

### Problem 2: how to return the encrypt or decrypt block as a string ###
this problem was solved as the initial code was being created by joining the blocks of encrypted and decrypted data with an empty string.  

## References ##
- Documentation of python : https://docs.python.org/3/
- Explanation of RSA Cryptography : https://www.youtube.com/playlist?list=PLRsutzRZu45_xPRS5ITFf_M_YpJxJRfV6
