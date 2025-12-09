Also known as SMTP, this protocol is designed to send emails from one mail server to another
It uses TCP port 25(This is a dangerous port since it's not encrpted). Port 465(more secured) and Port 587 are also used

Note this procotcol is s NOT used for downloading emails. 

Here are some commands

How  does SMTP work?
1. We write an email in an email app such as Gmail or outlook
2. Your email app connects to your outgoing SMTP server
3. This SMTP server processes the message
4. Using DNS Mail exchange records, it'll seek the destination sever.
5. The SMTP sever delivers the message to the destination server
6. Then finally the destination sever saves the email in the reciver's inbox. 

SMTP also has commands
Helo , starts the SMTP session on target client
Mail From  ,  points the senders email address
Rect to  , points to the reciever's email address
Data  , inficates that it's going to send the actually email. This is where we type in the message.
QUIT  //ends the session
