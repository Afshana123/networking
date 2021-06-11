# Networking

## What is a network?
A network is several devices that are connected to each other in order to exchange data 

## Network components
The main network component is the host. All computers that are connected to a network and participate directly in a network communication are classified hosts. Host refers to devices on the network that are assigned an address for communication purposes. Another term for host is an end-device.

Host = end-device

### Server-client architecture

Servers are computers with software that allow to provide information and services e.g. email, web pages to other end-devices on the network. In this case, it is a host also. A server is a host that provides a service.  

- client - a host that requests the service
- server - the host that is providing the service


main network component is the host(end-device which means the same thing):
- any computer that is connected to the computer and participating 
- should have an address 

### Peer-to-peer network architecture
This is usually where the client and server software run on separate computers but this time both can ask for services from one another

### Intermediary devices
These are the devices that connect the end devices to the network. The main idea of a network is to connect the host and end-devices. In order to do that, we use intermediary devices e.g. router 

These are in the network in order to connect the end-devices only. 

For example: firewall in order to protect the end device

They are there to connect end devices or to provide a function for these end-devices to be connected

## How to connect the network media?
Network media means the medium that we should to communicate between these devices. Modern networks primarily use 3 types of media to interconnect these devices:

- Metal wires(cables)
    - the normal cables that we use
    - e.g telephone wires
- Fibers
    - Fiber optics (you can have very high speed but there is a high cost)
- Wireless 
    - any wireless e.g. infrared, bluetooth, Wi-Fi, 5G, 4G anything
    - very easy but less secure than e.g. fiber-optic
    - easy to set up but hard to maintain because you get interference with other networks

## What network type do you use?
It depends on the parameter that you use to categorise the network. Sometimes we categorise the network based on:
- size of the area covered 
    - e.g. your network at home covers only your house which is different to a network that covers a whole building, or city or multi neighbourhoods
- number of users connected
    - e.g. you can have 10 users, you can have 10000 users
- type of services
    - e.g a network that provides an email service compared to a streaming network is different (they require different types of networks e.g you don't want delay when you are streaming)
- area of responsibility
    - when you are connected to the internet, you have a network at home or at a office  but also your network is connected to your providers network. Your network is your responsibility but your providers network is not your responsbility. 
    - when you are connected to the providers network, this connection is the boundary of your responsibility.
    - E.g. When you are connected to a WAN, you are responsible for the LAN and BT for example is responsible for LAN
      
## Common types of network infrastructure responsibility
- LAN - you have the responsibility of the network
- WAN - you are responsible for your LAN but not for WAN 

LAN - Local area Network
- A network infrastructure that allows access to users in small geographical areas e.g house, building, office etc. 

WAN - Wide Area Network
- that provides access to other networks over a wide geographical area which is typically owned or managed by a larger corporation or telecom provider
- e.g. internet 

MAN - Metro Area Network
- Not widely used 

Internet 
- Internet means interconnected network
- A worldwide collection of inter-connected networks 
- A connection of interconnected LANs and WANs e.g.  
- It is public

Intranet
- Refers to a private connection of LANs and WANs and is only accessible by the organisation
- It is private to the organisation
- only the authorised have access

Extranet 
- Not widely used
- provides a secure and safe access to individuals who work in different organisations 
- connects several organisations in one network
- It is still private 
- e.g. NHS - hospitals, clinics and trusts all work together 

## Communication fundamentals

There are three elements of communication:
- message source (sender)
- message destination (receiver)
- channel - source and destination will communicate over a channel 
      
The goal of communication is to transmit a message from the source to the destination over the channel. 
    
## Message delivery options
When you want to communicate and deliver a message, there are three options to deliver the message. The three options chosen depends on who is recieveing the message or how many parties are recieving the message. You can either deliver the message as a:

- unicast
  - when you say you want to deliver a message, it will only be delivered to only one destination
  - information being transmitted to a single end-device
- multicast 
  - message will be delivered to a set of destinations
  - We have several receivers in this case
  - information being transmitted to several end-devices
- broadcast
    - delivers the message to all destinations 
    - information being transmitted to all end-device

## Protocol suite or protocol standards:
A group of interrelated protocols necessary to perform a communication function. Each protocol performs a specific task. For example, we have a protocol to manage the network media (the network media in this case could be a wire, wireless or fiberoptic) and we have a protocol to make sure that the message has been delivered to the destination or we have a protocol to send emails. 

There are two main protocol suites for networking:
- OSI
  - Open System Interconnection Model
  - developed by ISO and ITU
- TCP IP 
 
### OSI Model Layer
There are 7 layers of the OSI Model and each one of these layers have a different set of protocols which means they all have a different function:

1. Physical layer
- defines the electrical and physical specifications of data connection
- responsible for transmission and reception unstructured raw data in a phsyical medium
- in this layer, we can define for example, the speed of the data
    
2. Data Link
- the layer that takes care of protocols
- describes methods for exchanging data between devices over the medium
- controls what happens in the physical layer
- for example, it describes how two hosts should communicate directly
- for layers 3-7, they do not care about the network media but data link layer will take it into account so that the above layers do not have to worry about it. For example, if you had a new type of wifi or faster type of ethernet, 3-7 will not change. 
    
3. Network layer
- the layer that provides services to allow end-devices to exchange data across networks
- if the hosts are not on the same network, the network layer will take of it
- e.g IP address is on the network layer
- one of the functionalities of a network layer is to give address to the hosts and routing 
- In order to determine which route to take, the network layer will take care of this
- concerned with delivering the data

4. Transport layer 
- concerned with checking whether the data has been delivered
- In this layer, we have two main protocols:
    - TCP: Transmission Control Protocol
      - will make sure that all the data will be delivered
      - sending an email - the email should be delivered in the same way on the recievers side
      - considered reliable and ensures that all data arrives at the destination
      -  
    - UDP: User Dataground Protocol
        - Some data is delivered but not all situations care whether the data has been delivered or not. e.g watching a live show and then you lost Bites then the screen or sound just goes off for a few second
        - Doesn't provide reliability and flow control but considered to be faster than TCP
    
Application Layer
choosing whether it will be TCP and UDP 
This layer includes:
5. Session layer
   -  When you want to send data, e.g when the client wants to request a service for the data
    you need to create a session 
      its a connection between the client and server or the sender and reciever
      authintecation process 
6. Presentation layer
   - considers the coding that is used, or the file types that are used
   - considers the way the data is formatted
    - considers the data that you are dealing with e.g picture, streaming, audio, whether the data is encripted etc 
7. Application layer 
    - ??
    
### TCP IP
Also known as the internet model.
- Network access layer 
    -where you define the protocols that will take care of the network media
    - controls the hardware devices and the media that make up the network
  
- Internet Layer 
    - The IP versions 
    - specificy the best path for the network and give IP addresses 
    
- Transport Layer 
  - supports the communication between various devices and defines whether they are connection oriented or connectionless
- Application Layer 
  - represents the data, the encoding and the control of the application protocol
- TCP/IP Layers 
    - includes all the protocols that are used e.g HTTP
    
How do these layers work together?
- Through encapsulation
- As application data is passed down, each protocol information will be added in each layer. 

## Port numbers 

In an IP address, when the traffic arrives at the host, the os needs to know which service this traffic should be directed to. This is why port numbers are used.

On each IP, we have port numbers from 0 to 65535 for TCP and UDP 
 
Why is it specifically this number (2^16)?
- Port numbers are addressed on 16 bits 
- This means that there are 65535 possible port numbers

Port numbers are managed by:
- Internet-Assigned Number Authority (IANA) 
    - responsible for these port numbers 
    - 0 to 1023: These port numbers are reserved for popular services and applications such as web services, web browsers, email clients, remote access etc
    - 1024 to 49151L These are registered ports primarily for applications that the user might need to install or for common applications 
    - 19152 to 65535: These port numbers are reserved for private or dynamic ports  

When it's done using the service or application, it will free the port again. 

Some well known ports: 
- TCP 20 - used by FTP (File Transfer Protocol): used to transfer data 
- TCP 21 - used by FTP: used to control data and establish the connection 
- TCP 22 - used by SSH (secure shell): this is the one we used to access the host 
- TCP 23 - Telnet is like SSH but it is not secure or encrypted 
- TCP 25 - SMTP (Simple mail transfer protocol)
- TCP 80 - used for HTTP (HyperText Transfer Protocol) for the web

## Bandwidth
- The bandwidth is the capacity at which the medium can carry data
- Digital bandwidth measures the amount of data that can flow from one place to another
- For example, the medium can carry up to 1 megabit per second
- Measured in bits per second, kilobits per second, megabits per second, gigabits per second and terabits per second

## Addressing 

Addressing is different depending on the layer we are talking about. When we talk about the network layer, we are referring to the IP Address. Data link addressing done using media access control (MAC) which has the MAC address. 

## MAC Address
The Mac Address is hardcoded in each network interface card so whenever you buy a network interface crad, it will come with its own MAC address. A MAC address is a global wide unique address which means you will not have two network interfcae cards that have the same MAC address. It is mainly given to the NIC when it is manufactured. 

### MAC Address - Data link addressing
- It is 48 bits which means if we take each 4 bits together, that means we have a 12 hexadecimal 
- The MAC addresses are read-only - they cannot be changed or modified but you can change them on the operating system. So you can ask the os to not use the MAC address from the NIC, you can set your own one instead. 
- You can check your MAC address on your machine by going on command prompt:
    - `ipconfig` - you will not be able to see the MAC address
    - `ipconfig /all` - you will get the MAC address or it might be under the name 'physical address'
- There are different MAC addresses for different interfaces 
- You can then check your NIC vendor (who made the card) from a quick search on google
- Not routeable - it never leaves the local network so you can't for example: search for it to see what country it's from 

## What do we mean by a positional numeral system?
- Base 10 means we have 10 different symbols in the numeral system
- Decimal numeral system or positional numeral system means that the digit represents different values depending on its position.

### IP Address - Network layer addressing
IP (Internet Protocol) Address:
- used to identify the host of any TCP IP network
- We have two version of IP addresses:
  - IPV4
  - IPV6

IPv4
  - A series of 1's and 0's
  - composed of 32 bits which equals 4 octets
  - 1 octet = 8 bits
  - We represent these using decimals
  - uses classful IP addressing - class A/B/C/D/E
  - classless IP addresses were introduced - they created a subnet mask 
    - they will give IP address and subnet mask
  - subnet mask
    - fixed the problem of the network and host portion
      - classful wasted a lot of IP addresses and having very huge networks 
      - so they changed the network portion to not be set to a fixed amount 
      - tell which portion represents network ID and host ID
    - series of ones, followed by series of zero's
    - the 1's represent the network ID
    - the 0's represent the host ID
    
IPv6
- When the internet began expanding at a faster rate, they started running out of addresses. This is why IPv6 was introduced.
- They added security features 
- composed of 128 bits 

you need to know whether two hosts are in the same network, or a different network - this is why this is useful 

Logical Operators

0 & 0 = 0, 
0 & 1 = 0,
1 & 0 = 0,
1 & 1 = 1

0 or 0 = 0,
0 or 1 = 1,
1 or 0 = 1,
1 or 1 = 1.

not 1 = 0,
not 0 = 1

IP Address:
- Every machine on the internet has a uniquie identifying number, called IP Address 

