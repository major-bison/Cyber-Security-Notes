The OSI Model was created as a standard for different computer networks to talk with each other. 
It breaks networking into 7 layers that assists us how data travels from one device to another.

**Layer 1 - Physical** 

The physical manifestation of network Connection. It refers to hardware and signals that they carry ( eletical wires, radio signals, Bluetooth, optical lasers) that uses binary digits
or in bits to transfer data. Examples include optical fiber cable, switch and router devices. 

What Layer 1 describes: Sending raw bits of 0 and 1 over a physical medium. It also defines voltages, frequencies and types of single. 
For cybersecurity, wire tapping (recording signals), jamming signals, and cutting off physical connections is considered a layer 1 attack

**Layer 2- Data Link Layer**

This layer deals with transferring data between devices that are on the same local network, meaning devices that are transferring from the switches, ethernet cables and wifi access point. It is the policy to talk over the signals. We can picture it as a local delivery system inside your office. 

Another important term to know is Network Segment: a group of computers that share the same network channel or are part of the same network group.  For example, 5 computers that are connected to a switch or in the same wifi.

The technologies in layer 2 have protocols such how the devices can relay information over a shared medium or channel. The number 802.11 represents wireless networks and for ethernet, it's 802.3 

At layer 2, we also have Mac addresses that are exclusively assigned to a device. A mac address contains 6 bytes (48 bits) and is written in hexadecimal. The format is AA:BB:CC:DD:EE:FF, and it is implemented in an exclusive network card. The first 3 bytes of a MAC address identify vendors/companies, and the last 3 bytes are special identifier of the device. Computer hackers love to manipulate Mac address all the time (spoofing)

At layer 2, data are being packaged into frames, adding source and destination of MAC addresses. Basic errors are also being detected here from the switch device. A switch is a device that identifies which port each computer device is available and forwards the frames to the designed computers or device. 

Cyber Security relevant in layer 2 involves Mac Spoofing, ARP Spoofing, and Rogue Access Points. 

ARP Spoofing, also known as ARP poisoning, occurs when a hacker tricks devices into sesnding traffic to them. 
ARP = Address Resolution Protocol, protocol that lets a computer find the MAC address of another device on the same local network. 

**Layer 3- Network Layer**

Into Layer 3, we have a layer thats responsible for sending data between different local networks.
This involves cities, countries or across the globe. 

In here, we have logical addressing (Assigning IP Addresses), Routing - choosing the safest and fastest path between networks and finally, Packet Forwarding - sending data that travels throughout the entire internet.

There are lot of protocols to know in this layer, including Internet Protocol, ICMP, Routing PRotocols, and VPN protocols. 

ICMP is a netework tool used for diagnositics such as ping and tracer route. 

In Cyber securiy relevance of layer 3




