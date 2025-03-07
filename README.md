# networksProject1
First project for the CS4220 Networks class 

Introduction
Understanding how to apply security to networking is a critical component of layered security
architecture. One method of applying security is by using protocols, such as Secure Sockets
Layer (SSL) or Transport Layer Security (TLS). In this project, you will create a simple secure
client and a secure web server to accept packets using OpenSSL.
Objectives
At the end of this project, students should be able to:
• Explain Secure Sockets Layer (SSL) and Transport Layer Security (TLS) protocols, including
their purpose in securing network communications.
• Create and utilize digital certificates to ensure SSL/TLS communication.
• Identify and troubleshoot issues related to SSL/TLS integration in network applications.
Instructions
1. Select your team in Canvas by self-assigning in the People section.
2. Use OpenSSL to implement SHA-256 to establish a TLS connection between the client and
server.
3. You will want to utilize the OpenSSL library
a. Tip --> check to see if it is installed: openssl version –a
b. Tip --> install if not listed: sudo apt install openssl
4. Develop an HTTP client in C.
5. Develop an HTTP server in C. The server should support only TLS 1.2 and higher. Disable all
non-secure protocols.
6. Create two digital certificates using OpenSSL's command-line tools (these can be self-
signed, if you want to utilize signed digital certificates through a free web service, you may
do that):
a. A server certificate signed with a private key and associated with the server's
hostname.
b. A client certificate signed with a client-side private key.
c. See below for resources on how to complete this task (the baeldung resource is
pretty good).
7. Ensure the TLS handshake performs mutual authentication (mTLS) often used in zero-trust
architecture.
8. Implement a secure key exchange mechanism during the TLS handshake to establish a
shared session key for encryption and decryption.
9. Use HMAC (Hash-based Message Authentication Code) to ensure data integrity.
10. Ensure you implement error handling throughout but pay special attention after OpenSSL
function calls.
11. Ensure the connection was successful by producing some sort of observable response
between the client and server. The communication does not necessarily need to be a file, it
could be text.
12. When the transmission is complete, the client should be disconnected from the server and
the connection should be closed.
13. Create a makefile to run your program.
Deliverables
1. A report called README.txt that includes (1) the full names of group members and the
statement: We/I have neither given nor received unauthorized assistance on this work; and
(2) a brief description about how you solved the problems you may have encountered and
what you learned.
2. A makfile to compile your program.
3. Upload a copy of your source code to Canvas.
README.txt
Write a README.txt file that explains how to build and run your program, gives a brief
description of the pieces of your assignment, identifies any challenges you overcame, and
contains any notes about resources you used or discussions you had with others. I suggest
starting work on your assignment with this file and maintaining it as you work.
COMMENT YOUR CODE. If something does not work, you will get partial credit if your
comments show that you were thinking logically to solve the problem. Document any places
where you received help from others. Essential elements of the grading will include the
elegance of your implementation and documentation, for correctness, and efficiency.
Resources
Baeldung. (2024). Creating a Self-Signed Certificate With OpenSSL.
https://www.baeldung.com/openssl-self-signed-cert
Khlebnikov, A. (2022). Demystifying Cryptography with OpenSSL 3.0. O’Reilly.
https://learning.oreilly.com/library/view/demystifying-cryptography-
with/9781800560345/B16767_10_Final_AM.xhtml#_idParaDest-198
OpenSSL: https://www.openssl.org/
Tanenbaum, A. S., Feamster, N., and Wetherall, D. (2021). Computer networks. Pearson.
Sections: 6.1.3 Berkeley Sockets; 6.1.4 An Example of Socket Programming: An Internet
File
Server; 6.5.2 The TCP Service Model; 3.4.2 A Protocol Using Go-Back-N; and review
accumulative acknowledgement.
Van Winkle, L. (2019). Hands-on network programming with C. Pakt Publishing.
Found in the O’Reilly database through the UCCS Kraemer Library. See: Section 3 -
Understanding Encrypted Protocols and OpenSSL
