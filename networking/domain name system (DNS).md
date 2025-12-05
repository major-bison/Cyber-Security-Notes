What is a Domain Name system?

DNS is basically the system that translates domain names into IP addresses. It mostly uses UDP port 53 because it’s fast, but it switches to TCP 53 when the data is large or for zone transfers. 
  
   DNS has different record types: A and AAAA for IP mapping, CNAME for aliases, MX for email, TXT for extra info.
For security work, DNS is super important because attackers constantly abuse it. 
They do DNS tunneling to sneak data out, fast-flux to rotate IPs, cache poisoning, and hijacking.  
Malware often uses DNS to find command-and-control servers or uses DGAs to generate tons of random domains.  
As a SOC analyst, you monitor DNS logs for strange patterns. 

1.An A record connects a domain name to an IPv4 address. Basically, it tells the internet “this website lives at this exact IP.” 

2.A AAAA record does the same thing as an A record, but for IPv6 instead of IPv4. It’s just the IPv6 version of mapping a domain to its address.

3.A CNAME record makes one domain point to another domain. It’s like an alias, when you type one name, it actually takes you to the real, main domain behind it.

4.An MX record tells the internet which mail server should handle emails for a domain. If someone sends mail to a domain, the MX record decides where that email goes.
