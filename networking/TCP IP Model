The TCP/IP Model is the practical and current, real-world networking model used by the entire internet.
While the OSI Model is more of a conceptual framework, the TCP/IP model is the actual model computers and routers follow when sending data today.

TCP/IP stands for:
TCP — Transmission Control Protocol
IP — Internet Protocol

These are the two core protocols that form the basis of internet communication.
Developed by The U.S. Department of Defense in the 1970s to make large networks more reliable, 
decentralized and manageable/control, and able to keep working even if parts of the network failed.

Unlike the OSI model (7 layers), the TCP/IP model has 4 layers:

1. Application Layer
This merges OSI layers 5, 6, and 7.
This is where applications communicate.
Protocols:

HTTP / HTTPS
DNS
SSH
FTP
SMTP / IMAP / POP3
Telnet
This layer is what your apps use to talk to the network.

2. Transport Layer
Same as OSI Layer 4.
Responsible for end-to-end communication and port numbers.
Protocols:

TCP (reliable)
UDP (fast, no reliability)

This layer makes sure data is delivered to the right application

3. Internet Layer

Equivalent to OSI Layer 3 (Network Layer).

Handles:
IP addresses
Routing
Packet forwarding
Path selection

Protocols:

IP (IPv4 / IPv6)
ICMP (ping)
IPSec
ARP 
This is the layer that connects networks worldwide.

4. Network Access Layer / Link Layer

This combines OSI Layer 1 and Layer 2.

Handles:
MAC addresses
Ethernet
WiFi
Frames
Physical signals
Protocols/technologies:
Ethernet 802.3
WiFi 802.11
ARP
Switches, NICs, etc.

This is where the actual physical transmission happens.

Everything we use online runs on these four layers.
Understanding how they work helps you read packet captures in Wireshark, use tools like Nmap and tcpdump, and understand where attacks happen.

Cybersecurity attacks often target specific layers:

Layer 4 → SYN floods, UDP floods
Layer 3 → IP spoofing, ICMP attacks
Laye 7 → web attacks (SQL injection, XSS, etc.)
Layer 1 & 2 (inside Link Layer) → ARP spoofing, MAC spoofing

Knowing the TCP/IP model makes it way easier to understand how networks operate in real-world environments.
