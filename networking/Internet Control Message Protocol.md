ICMP means Internet Control Message Protocol.

Note that ICMP is not a program, not an application, not a service, and not a port-based protocol like TCP or UDP.
What ICMP actually is, it's a messaging protocol built into the IP layer (Layer 3).

Its job is to let devices send control messages to each other about what’s happening on the network.
Think of ICMP as the network’s feedback system.

Each ICMP message has:
Type: what kind of message (e.g., echo request = 8, echo reply = 0)
Code: extra details about the type
Checksum: error detection
Data: depends on the message, often includes the IP header + part of the original packet
