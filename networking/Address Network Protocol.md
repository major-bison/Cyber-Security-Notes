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


![ARP Wireshark](https://github.com/chgonzaga1/malware-engineering/blob/main/image-of-cpu-register.jpg)



Let's take a look of a screenshot
Through the use of Wireshark, we can take a closer look of what's going on during a ARP request.

![TCP Dump 1](networking/images/tcpdump1.png)


