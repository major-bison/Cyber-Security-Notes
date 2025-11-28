Unicast means sending data from one device directly to one specific device on a network.
It’s a one-to-one communication: one sender, one receiver.

Example:
Your computer sending a message only to your friend’s computer.

Multicast means sending data from one device to a selected group of devices on the network.
It’s a one-to-many communication  but only to devices that are part of that specific group, not to everyone, 

Broadcoast means to ALL Recievers 

A broadcast domain is a “zone” in a network where broadcast messages can reach all devices. A router is a device that seperates domains. 


A collision domain is a section of a network where data packets can “collide” with each other because they share the same communication path.

On a hub, everything is shared.
Any packet sent in one port is sent out of every port.
Because of this, the entire hub is one big collision domain.

On a switch, it’s different.
Switches send data only to the device it’s meant for.
This means each switch port is its own collision domain, which prevents collisions.

A subnet mask is a number that that indicates a device which part of an IP address, is the **network** and which part is the **host.**
You need a subnet mask because without it, devices can’t find the network and can’t communicate, properly. Subnet masks are 4 bytes.

Every IP address class has a default subnet mask
Class A → 255.0.0.0 (/8)
Class B → 255.255.0.0 (/16)
Class C → 255.255.255.0 (/24)

The (/8), (/16), (/24) indicates how many 11111111s are there in a 4 byte, and it's the 11111111 that masking the net

ex) 11111111 00000000 00000000 00000000 = 255.0.0.0

Here's an example how subnet masks are being used:
A debvce has an IP Address of  192.168.1.20 and a subnet mask of 255.255.255.0 (/24)
A router might ask, What part is the network? using the subnet mask, 

The 255s tell you that 191.168.1 are the network part, hence 255.255.255.x
while x.x.x.20 is the host part 

Calcuating The Network Address with a Subnet:

To figure out the network address of an IP, you compare the IP address and the subnet mask bit by bit using a rule called a bitwise AND.
When you AND the two together, the final result tells you which network that IP belongs to.

We will need to use THE AND rules in order to calculate the binary number.
1 AND 1 = 1
1 and 0 = 0
0 and 1 = 0
0 and 0 = 0

for example) ): 192.168.3.100, converting this to a binary number, we get : 11000000.10101000.00000011.01100100
The Subnet mask is 11111111.11111111.11111111.00000000

With both values, we will use the AND operation to find it's Network Part address
11000000.10101000.00000011.01100100
11111111.11111111.11111111.00000000
-----------------------------------
11000000.10101000.00000011.00000000 <- this is the answer now

11000000.10101000.00000011.00000000 convert this back to decimal and we get 192.168.3.0

Thus 192.168.3.0 is the network address for 192.168.3.100


For linux and macOS machines, we can use ifconfig to get the ip address and mac address as well of the device. For Windows, it's ipconfig. 

**PRIVATE IP ADDRESS AND NETWORK ADDRESS TRANSLATION**

Private IPs are special IP ranges that are not routable on the public internet.
They are used inside local networks only, such as:
Your home Wi-Fi network
School or office networks
On-premises corporate networks
Internal VLANs in enterprise SOC environments

Devices inside these networks talk with each other using these private addresses.
To access the internet, these devices use NAT (Network Address Translation) on a router.

These ranges are defined by RFC 1918:
**10.0.0.0 – 10.255.255.255**

The largest private range are often used in large organizations, cloud environments, AWS VPCs, Azure VNets
It can support millions of hosts

172.16.0.0 – 172.31.255.255
Medium-sized range
Used in medium to large businesses

Avoids conflicts with the common 192.168.x.x networks
 192.168.0.0 – 192.168.255.255
The most common for home networks
Wi-Fi routers typically use:
192.168.0.x
192.168.1.x

Inbound traffic from the internet should never contain private IPs → indicates spoofing
Know which subnets belong to which departments in an enterprise
Helps identify lateral movement in breaches

Now then, What Is NAT?

NAT = Network Address Translation, a special feature of a router
It’s the process your router uses to translate private IPs into a public IP so your devices can use the internet.
Note that Private IP addresses should not be going outbound. 
