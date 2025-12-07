In this section, I will be providing details about HTTP and HTTPS

HTTP known as Hypertext transfer protocol is used as a general protocol that applied to community with web servers.  
It defines: How your brwowsers requests fora web page, how the server will respond and how the data will present like  
which includes headers, status codes and content of the page.

Each request is independent meaning it doesnt remember previous requests unless cookies, sessions
or tokens are applied. However it is not secured. 

Hackers can just intercept, read or modify the traffic. (Man in the middle attack)
It is not recommended to type a password over a HTTP 

So it's recommended to HTTPS.

HTTPS, the s stands for secure, which is basically HTTP with TLS encryption, Transport Layer Security
In here, the data is scrambled. It also has an authnetication, meanign the server
has a certificate from a trusted authority, meaning you're communication with an authnetic website.  

Data also cannot be modified in transit without detection.

The ports for HTTP is 80 and HTTPS 443. Another alternative port for HTTPS is 8443.  

HTTP METHODS: GET, POST, PUT, DELETE

//EXPLAIN THESE METHODS NEXT

HTTP methods are basically the actions your browser or an app asks a web server to do.  
Every time you click a link, submit a form, upload something, or delete something online,   
one of these methods is being used behind the scenes.  

1)Get: 

Used to retrieve information from a server.  
This is what happens when you open a webpage or load an image.  
It never changes data on the server—it's only reading, not modifying.  
An example would be: GET /profile/chris after you go to a link www.lalafacebook/profile/bison

2)Post:

Applied when you send data to the server.
It is common for logging in, submitting forms, uploading files  
Data goes in the request body, not into the URL

3)Put

4)Delete 

5)Patch

6)Head

7)Options
