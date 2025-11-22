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

In Cyber security, the relevance of layer 3
-IP Spoofing, Attackers fake their IP addresses to stay hidden in the internet
-ICMP Attacks
-Routing Attacks, hijacking routing protocols to misdirect traffic into another server
-Using Man in the Middle tickets for routing manipulating. If attackers an influcnce routing tables/records, they can intercept traffic. 

**Layer 4 Transpor Layer****
Layer 4 is responsible for end-to-end communication between applications.
It ensures that data is delivered reliably (or quickly, depending on the protocol).

While Layer 3 gets the packet to the correct network, Layer 4 gets it to the correct application on the destination device.

Think of Layer 3 as mailing a package to the right building.
Layer 4 makes sure it gets delivered to the right apartment inside the building.

A layer 4, port numbers are identified here for application to recieve data

Port 80 belongs to HTTP, Port 443 is the secure one
SSH belongs to SSH

At the Transport layer 4 layer,
it also decides whethere data should have error check regulation but slow or no guaranntee to be deliever but quick
Segementation also occurs here including flow control management(making sure that the reciever is not over whelmed)

There Two Main Transport Layer protocols, TCP and UDP, which I discussed earelier.
TCP involves guaranteed delivery, ordered data, error checking, retransmissions and 3 way handshake.
TCP based services include HTTPS, SSH, FTP, and Email.

UDP involves quick delivery but not guarantee delievery, no order, and very low latency.
Online Gaming, Streaming and VoIP are examples of UDP. 

In Cyber Security layer 4 attacks, it involves SYN Flood, Attackers send many TCP SYN (part of 3 hard shake) packets to exhaust reserouces. UDP flood is similar as well.  Attacks can manipulation TCP flags as well to overwhelm firewalls. 


**Layer 5 Session**

It is basically the part of networking that keeps a conversation going between two devices. When two applications want to talk, the session layer is what starts that connection, keeps it open, and makes sure everything stays in order while data is being exchanged. If the connection drops or pauses, this layer helps pick things back up without starting over. You can think of it as the “meeting organizer” that handles when a session begins, stays active, and ends. This matters in cybersecurity because a lot of attacks target sessions, like stealing someone’s login session, hijacking a web cookie, or abusing a VPN session. If a session isn’t protected or expires properly, attackers can slip in and impersonate a user.

Session Layer also involves keeping SSH Session stable, world of warcraft servers able to host players or staying logged in with your email account. Also Session layers keep the connection or the sesession alive such as a video call that freeses but able to resume few seconds later.


Layer 6 is basically the “formatting and translating” layer of the OSI Model. Its main job is to make sure the data being sent from one device can actually be understood by the application on the other device. Different systems use different formats, so the presentation layer acts like the middleman that converts things into a standard form.

This layer handles three important things:
1. Encoding
This includes character sets (ASCII, UTF-8, Unicode) and file formats (JPEG, PNG, MP3, AVI). It ensures that text, images, audio, and video are represented in a way that both sides recognize.

2. Compression
Large files (videos, images, documents) are often compressed so they travel faster across the network. This is handled at Layer 6.

3. Encryption / Decryption
This is one of the biggest security roles of Layer 6. Whenever you use HTTPS, TLS, SSL, or certificates, encryption happens here. Your data is scrambled into a secure format before transmission—and decoded on the receiving side.

A good example is emailing a photo. The image is saved as JPEG or PNG (Layer 6 format). When the email client attaches it, something like MIME converts it into a safe, standardized format so it can be transmitted over the internet.

In layer 6, malware can be compressed into paylods. PDFs and Images can be used to hide with malicous intent

Layer 7 is the final layer. The part you actually interact with as a user. This layer contains the network services your applications use every day, such as web browsing, email, file transfers, messaging, DNS lookups, and more.
Any time you type a URL into your browser, send an email, watch a video, or play an online game, you’re using Layer 7 protocols.

Examples include:

HTTP / HTTPS which is for web browsing
DNS converts domain names to IP addresses

HTTP Floods/Layer 7 DDos occurs here and DNS poision as well
