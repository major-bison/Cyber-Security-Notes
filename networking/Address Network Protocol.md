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
