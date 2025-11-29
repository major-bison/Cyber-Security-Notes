



1. What is TTL? (Time To Live)

TTL is a number in the IP header that prevents packets from looping forever.
Every time a packet passes through a router, the router decreases TTL by 1.
If TTL reaches 0, the router drops the packet.
This prevents infinite routing loops.

Example:
TTL = 64 (common on Linux)
After 5 routers → TTL = 59

A very low TTL may indicate malware beaconing.
TTL values help identify OS fingerprinting (e.g., Windows default = 128, Linux = 64).

Malware Beaconing : when infected devices regularly send small “check-in” messages to an attacker’s command-and-control server.

2. What is Checksum (and Checksum Updates)?

A checksum is a small value used to check for errors in the header.
When a packet goes through a router:
The router modifies parts of the IP header (like TTL).
Because of that, the checksum must be recalculated.
The router updates it before sending the packet forward.
If the checksum is wrong → packet is considered corrupted and is dropped.

In cybersecurity:
Attackers sometimes intentionally corrupt checksums to evade detection or confuse IDS systems.
Analysts often check checksums in PCAPs to confirm packet integrity.

3. What is Fragmentation?

Fragmentation happens when a packet is too large to pass through a network with a smaller MTU (Maximum Transmission Unit).

Example:
Ethernet MTU = 1500 bytes
If a packet is 3000 bytes → it must be split into smaller pieces.
Routers break the packet into smaller fragments, each with:
Its own header
Offset values to help the receiving device reassemble them

In cybersecurity:

Attackers can use fragmentation attacks to hide malicious payloads across fragments.
IDS/IPS must reassemble fragments to detect threats.
Misconfigured MTU values cause packet loss.

4. What are TCP Flags (SYN, ACK, etc.)?

TCP flags are 1-bit indicators inside the TCP header that describe what kind of message the packet is.
Here are the most important ones:

Flag	Meaning
SYN	Start a new TCP connection
ACK	Acknowledge received data
FIN	End a connection
RST	Reset/abort a connection
PSH	Push data immediately
URG	Urgent data

These flags make TCP reliable.

In cybersecurity:
SYN floods = DDoS attack
XMAS scans = FIN + PSH + URG
NULL scan = no flags
FIN scan = only FIN
Firewall rules often inspect TCP flags
IDS tools like Snort look for odd flag combinations

5. What is a Sequence Number?

TCP breaks data into small chunks called segments.
Each segment needs a number so the receiver knows the correct order.

A sequence number identifies:
Which piece of data this segment contains
Where it fits in the stream
Which datahas been successfully received

Example:
Sender → sends 1,000 bytes
Sequence number: 1
Next segment: sequence number 1001
The receiver sends back ACK 1001, meaning "I got everything up through 1000."

In cybersecurity:

Sequence numbers protect against packet duplication
Attackers sometimes attempt sequence number prediction to hijack connections (old TCP hijacking attacks)
