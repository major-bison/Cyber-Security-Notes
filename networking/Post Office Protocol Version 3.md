Post Office Protocol v3 also known as POP3

It's a protocol that is designed for email clients to download emails from a mail server. 
WOrks on TCP port 110 and the secure version works on TCP port 995

POP3 can also store emails on a local computer. 

Using a TCP connection to a POP3 server, we can connected to it after authenticate your username and password   

From there, we can list messages, download, delete and check how many messages exist.

Here are list of commands:
Command	Meaning
USER <username> -	Identify the user  
PASS <password> -	Provide password  
STAT -	Get number of messages + total size  
LIST -	List messages with sizes  
RETR  -	Download the message  
DELE -	Mark message for deletion  
QUIT -	Close session and apply deletes  
