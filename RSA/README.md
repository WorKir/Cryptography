# RSA

## Purpose and main tasks of the work
Acquaintance with tests for verifying numbers for simplicity and key generation methods for an asymmetric cryptosystem of the RSA type; practical familiarization with the information protection system based on the RSA cryptosystem, organization using this system of classified communication and electronic signature, study of the key distribution protocol.

## Task
Implement mechanisms for checking numbers for simplicity, using them to find pairs of prime numbers and implement the RSA algorithm. Exchange keys using the RSA protocol/

## Progress

- Implementation and testing of functions for finding prime numbers
- Implementation of a custom class with methods that perform encryption with the RSA algorithm.
- Implementation of high-level functions for working with the site

The difficulties that arose were related to the algorithm for finding prime numbers and connecting to the site.
Difficulties are solved by analyzing and testing each function separately from the others.

## Description of the steps of the confidential key distribution protocol
Subscriber A(d, n, e) forms a message (k, S) and sends it to B(d1, n1, e1), where
k1 = k^e1 mod n1
S1 = S^e1 mod n1
S = k^d mod n

Subscriber B finds (confidentiality) with the help of his secret key d1:
k = k1^d1 mod n1
S = S1^d1 mod n1

And with the help of the public key e of the subscriber A checks the signature of A (authentication):
k = S^e mod n
