ICMP means Internet Control Message Protocol.

Note that ICMP is not a program, not an application, not a service, and not a port-based protocol like TCP or UDP.
What ICMP actually is, it's a messaging protocol built into the IP layer (Layer 3).

Its job is to let devices send control messages to each other about what’s happening on the network.
We can think of ICMP as the network’s feedback system.

Each ICMP message has:
Type: what kind of message (e.g., echo request = 8, echo reply = 0)

Code: extra details about the type

Checksum: error detection

Data: depends on the message, often includes the IP header + part of the original packet


What Ping Actually Checks

Connectivity

Reachability

Round-Trip Time (RTT): How long it took the packet to go from you → target → back to you.

Packet Loss: How many pings get lost or dropped.

Latency & Stability: High variability (jitter) = unstable network.

Also, an Echo Request is a special kind of ICMP packet sent when you use the ping command.
It contains, ICMP Type 8, ICMP Code 0, Identifier (ID) ,Sequence number (#1, #2, #3…), A checksum, Optional data (ping's payload, usually 32 bytes)
Type 8 means echo request, Typ 0 means echo response
The code means 
