What is Adress Network Protocol (ARP)

ARP is a protocol that's installed inside every operating system and every network device. It runs automatically inside the networking stack. 
Devices strickly always need a Mac address to talk to each other. DHCP does not do that, it's the ARP that performs this. 
Devices cannot simply send traffic until it learns the router’s MAC.

It doesn’t just live inside the router. Every device on the local network uses ARP including laptops, my smart phone, the router, and other computer devices.
Anytime a device wants to talk to another device on the same network, it first has to ARP to learn the other device’s MAC address.

If my laptop wants to talk to the router, it sends an ARP Request asking:
“Who has this IP? What’s your MAC address?”
The router replies with its MAC, and now both sides know how to send Ethernet frames to each other.
Same thing if two computers on the same LAN want to talk. They ARP each other directly without the router getting involved.

ARP only works inside the local network (not over the internet). Without ARP, no device could send or receive anything at Layer 2.

//Insert a picture of Arp Spoofing
Now what is ARP Spoofing? 

ARP spoofing occurs when an attacker lies on the network by sending fake ARP replies. The goal is to trick devices into thinking the attacker’s MAC address belongs to another important IP, usually the router or another victim.

Basically, the attacker says:

“I’m that other device you’re trying to reach.”
Once devices believe the attacker, all the traffic that should go between the victim and the router gets rerouted through the attacker first. 
This enables the attacker to 

1. Read the victim’s traffic
2. Ateal logins and cookies
3. Modify packets
4. Inject malware
4. Break connections
5. DoS a device by sending bogus ARP entries

ARP spoofing works because ARP has no authentication, meaning devices trust whatever ARP reply they receive.


![ARP Wireshark](https://github.com/chgonzaga1/Cyber-Security-Notes/blob/main/networking/images/arpwireshark.png)

Note: Wireshark is a network analyzer tool used by Network technicians to examine and capture network packets, decode and analyze them. 


Let's take a look of a screenshot
Through the use of Wireshark, we can take a closer look of what's going on during a ARP request.

The screenshot shows how Wireshark displays a packet using two different views.
The top panel shows the human-readable, decoded information, like the source and destination MAC addresses, the protocol type (IPv4), and the higher level protocol layers such as TCP and TLS.
The bottom panel shows the raw packet bytes, which are the actual binary data captured on the wire. These bytes are represented in hexadecimal. The destination MAC, source MAC, and EtherType (0800 for IPv4) in the bottom panel directly match the decoded fields in the top panel.
In other words, the top panel explains what the packet means, and the bottom panel shows what the packet actually looks like in raw form.

![TCP Dump 1](https://github.com/chgonzaga1/Cyber-Security-Notes/blob/main/networking/images/tcpdump1.png)

Now using the following command lines: tshark -r arp.pcapng -Nn
                                       tcpdump -r arp.pcapng -n -v

We can use them to check what's going on when ARP is identifying the IP address:
tshark -r arp.pcapng -Nn:
1. tshark is a command for wireshark
2. The arugment -r is used read from a file
3. arp.pcapng is the name of the file. 


