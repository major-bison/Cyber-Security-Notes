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

When I type a website, my computer first checks if it already knows the IP from its cache or hosts file. If not, it sends a DNS request to a DNS server (usually my router, ISP, or work DNS) on UDP port 53 asking for the A record of that domain.

If that DNS server doesn’t have it cached, it goes up the chain: first the root servers, then the .com servers, then the domain’s authoritative DNS server, until it finally gets the real IP. That IP is sent back to my computer, cached, and then my browser uses that IP to make a normal TCP connection (like HTTPS on 443) to load the website.

So note getting a IP address for the website requries to go thruough many layers of DNS servers

1) A root server is the top-level DNS server. It doesn’t know the website’s IP but tells you where to find the .com servers or the TLD servers

2)The .com TLD servers also don’t know the IP, but they know which DNS servers handle that specific domain.

3)The authoritative DNS server is the one that actually knows the real IP address of the website.

YSo es, DNS goes through multiple DNS servers in a chain. Each one points you to the next until you get the final answer.

Once the resolver has the answer, it caches it so you don’t have to repeat all those steps next time.

We will now take a look at nslookup command line, which retrives the IP address of a domain.  

