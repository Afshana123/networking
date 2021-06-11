# Main Four Protocls 

All are application layer protocols

Whenever a protocol uses a port it listens to, it means it is on the application layer

## DHCP Server

DHCP: Dynamic Host Configuration Protocol

Functionality:
- To give configuration to the host e.g IP addresses and default gateways were defined to the hosts
- When you have multiple hosts, DHCP solves the problem by just giving the configuration to the host dynamically.
- This is a server-client protocol where the server will give the configuration to the client 
- It will broadcast on the network and wait for the configuration to be sent
- The configuration is like a lease, the client will need to renew the configuration after some time and take a new configuration 
- works on broadcast mode, the host in the network has no idea who the DHCP server is so it will broadcast the request asking for an IP request  

If there is not a server, the hosts, in this case the PCs will take a random IP address in order to keep communicating if they have to - you just do `ipconfig` in the command prompt and set to DHCP 

DHCP works on the application layer protocol - because it's udp is on the application layer but it's used to give IP addresses to other hosts.
 

Only works on UDP, not TCP 

Port numbers:
- 67 for the server side
- 68 for the client side 

`ipconfig /renew` - it will renew the IP address
`ipconfig /release` - the host does not have any IP address


## HTTP Server 

HyperText Transfer Protocol in an application layer protocol for transmitting hyper media documents such as HTML files or documents.

HTML is a markup language e.g pictures, word documents 

HTTP was designed for the communication between the web server and web browser (the web-server is the server and web browser is the client that will ask and communicate with the web-server)

It is a client-server protocol.

Client send the request and server recieves the request and sends a response

works on TCP

Port number:
works on TCP 80 - HTTP
TCP 443 - HTTPS 

http - information is exchanged without default
https - information is encripted - secure 


## FTP Server 

File transfer protocol is the standard internet protocol for for transmitting files between computers

It uses TCP 

It uses two ports:
-port 20
    - used to transfer data 
-port 21
    - used to control data (to establish a connection between client and server)

It is client server protocol also

When you download a file from your computer, you are not using FTP but you are transferring the file using HTTP/HTTPS but if you want something efficient and something which was designed to transfer files, you would use FTP.

`dir` - checks the files we have on the server

## DNS 

Domain Name Systems 

Usually in real-life, we don't use an IP address, you use a name

DNS maps URL names to IP addresses 

Note that IP addresses can change for example: bbc does not have only one server

There is a hierarchy system for DNS 

The host realises they are dealing with a name 

DNS is not a broadcast protocol - it sends the packet directly to the server 

DNS Query is asking what the name of the IP address is for the www.cyber.com
DNS Answer replies back with the IP address


DNS has to be on the same broadcast - FTF, HTTP and DHCP does not need to be in the same broadcast 

DNS works on UDP 

Why does it work on UDP? 
It's a small request so if you lost the request, it is easier to ask for the same information again than to keep making sure that you recieved the reply for the request. 

Port:
53


