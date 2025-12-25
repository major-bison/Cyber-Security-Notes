
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

e) SSH allows graphical applications from a remote Unix-like system to be displayed and used locally.

ssh username@host to use SSH command line

-SFTP-

SFTP (SSH File Transfer Protocol) is a secure way to transfer files that runs over SSH and uses port 22.  
It’s part of the SSH suite, so once SFTP is enabled on an OpenSSH server, you can connect with a command like sftp username@hostname and upload or download files using simple Unix-style commands such as get and put.  

SFTP is often confused with FTPS, but they are different technologies. FTPS (File Transfer Protocol Secure) is FTP secured with TLS, similar to how HTTPS secures HTTP.   

FTPS typically uses port 990, requires TLS certificates, and can be harder to configure through strict firewalls because it uses separate control and data connections.  

Overall, SFTP is easier to set up and manage since it only requires SSH, whereas FTPS relies on TLS certificates and more complex networking rules, similar to other TLS-secured protocols such as HTTPS or IMAPS.  

-VPN-

VPN Architecture and Traffic Flow Overview

A VPN allows remote offices or users to securely connect to a main branch network as if they were physically on-site (but they're remotely) . In a typical setup, a VPN server is located at the main branch, while VPN clients are used by remote branches or individual users. Once connected, a secure encrypted tunnel is established over the Internet.  

In a site-to-site VPN, entire remote networks connect to the main branch. All devices at the remote office send their traffic through a VPN gateway, which encrypts the data before sending it across the Internet. The encrypted traffic travels through the VPN tunnel and is decrypted only after reaching the main branch network.  

In a remote access VPN, individual users connect directly to the main branch using a VPN client on their device. This setup is common for remote workers and provides secure access to internal resources without exposing traffic to the public Internet.  

**VPN Tunneling and Internet Traffic Behavior**

Once a VPN tunnel is established, most or all Internet traffic is routed through the VPN server. As a result:

External websites and services see the VPN server’s public IP address, not the user’s real IP.

The local ISP can only see encrypted traffic, limiting its ability to inspect or censor activity.

This behavior is often used to bypass geographical restrictions.

For example, if a user connects to a VPN server located in Japan, websites will treat the user as if they are physically in Japan and may automatically serve region-specific content (such as a Japanese version of a website).

Important Considerations:

Not all VPNs route all traffic through the tunnel. Some are configured only to allow access to private internal networks (split tunneling).  

Some VPN servers may leak the user’s real IP address if misconfigured, so verification tests (such as DNS leak tests) are recommended.  

VPN usage may be restricted or illegal in certain countries, so local laws should always be checked before using a VPN.  
