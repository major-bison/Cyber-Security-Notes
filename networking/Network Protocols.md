
TLS is a transport-layer cryptographic protocol that ensures confidentiality and integrity by encrypting data between a client and server, 
protecting it from packet sniffing and tampering on insecure networks.

TLS provides two main guarantees: 1) Confidentiality and 2) Integrity  

1) External people should not be able to access your data and it's also encryped.  
2) With integrity, no one can modify the data and tampering is usually detected

Without TLS, Online shopping and banking would be unsafe to use. Emails and text messages could be altered or read  

HTTPS, IMAPS, POP3S are an examples of TLS protocol being implemented.  

It's essential to note that encryption without identity verification would still permit man-in-the-middle (MITM) attacks.   
That’s where TLS certificates and Certificate Authorities (CAs) are implemented.  

A TLS certificate confirms the authenticity of the server’s identity, its public key, and a trusted authority that vouches for it

The certificate creation process: 

1) Server creates a CSR  
The server admin generates a Certificate Signing Request (CSR)
The CSR contains: Domain name, Public key, Organization info

2) CSR is sent to a Certificate Authority (CA)   
Examples of CAs:   
DigiCert   
GlobalSign   
Let’s Encrypt   
Sectigo    
3) CA verifies the request  

Confirms domain ownership and performs identity checks (depending on cert type)  

Step 4) CA issues a signed certificate    

The CA digitally signs the certificate and this signature is what browsers later verify  


-SSH-

Telnet made it easy to manage systems remotely, but it had a major security flaw: all data, including usernames and passwords, was sent in cleartext. This meant anyone monitoring network traffic could easily steal login credentials. Thus, Secure Shell (SSH) was created.  

SSH was developed by Tatu Ylönen in 1995, then in 1999, the OpenBSD team introduced OpenSSH, an open-source implementation of SSH that is now the foundation for most modern SSH clients.

Key Benefits of OpenSSH :

a)Secure Authentication  
SSH supports multiple authentication methods, including passwords, public-key authentication, and even two-factor authentication. 

b) Confidentiality
All communication is encrypted end-to-end, preventing eavesdropping. SSH also warns users when a server’s key changes, helping detect man-in-the-middle attacks.  

c) Integrity
Cryptographic checks ensure that data is not altered while being transmitted.  

d) Tunneling  
SSH can securely forward other network protocols, creating a VPN-like encrypted tunnel.  
