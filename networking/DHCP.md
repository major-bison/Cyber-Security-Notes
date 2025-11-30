DHCP (Dynamic Host Configuration Protocol)

is a network service that automatically assigns IP configuration to devices so they can join a network automatically

When your smart phone, laptop, or smart TV connects to Wi-Fi, they require a 
1.IP address
2.Subnet mask
3.Default gateway
4.DNS servers

They also needlease time, domain name, WINS servers, etc.

Instead of typing all this manually into the network configuration, the DHCP server gives it to you automatically when connected to the WiFi.

DHCP runs at the Application-layer protocol, layer 7 of the OSI model. It's a service protocol and it uses User Datagram Protocol
UDP is lightweight and it has no connection handshake, meaning it looks for speed.
DHCP is usually setup already before it connects wifi
DHCP server listens on UDP port 67 and DHCP client uses  UDP port 68
Your device sends from port 68 to server on port 67.

DHCP’s job is to automatically hand out network configuration to devices.

So to review, DHCP assigns:
IP Address: The unique number your device needs on the network.
Subnet Mask: Defines what network you belong to.
Default Gateway: The router that sends your traffic to other networks (like the internet).
DNS Server: Translates website names (google.com) to IPs.
Lease Time: How long you can keep the IP before renewal.

The DORA Process (The meat of DHCP)
DHCP works through a famous four-step conversation between client and server:

1. Discover
Client broadcasts:
“Hello there, Is there any DHCP server out there?”

2. Offer
A server replies:
“I can give you an IP address nwo. Here’s my offer.”

3. Request
Client replies: “Yes, I want that IP.”

4. Acknowledge
Server says:
“Complete, so this IP address is yours.”
After this, the device is ready to communicate on the network.

NOTE: Usually the router is your DHCP server. 



