Problem

Task was to connect to the server jupiter.challenges.picoctf.org at port 41120 using the netcat (nc) tool to retrieve the flag.

Solution 

Netcat is a powerful networking utility that allows for reading and writing data across network connections using TCP or UDP protocols.

To solve this, I first researched how to use netcat to establish a connection to a specific server and port.

The syntax I used was nc [hostname] [port], and 

in this case, I ran the command nc jupiter.challenges.picoctf.org 41120.

This successfully connected me to the server, where I was greeted with a prompt or message that included the flag. 
