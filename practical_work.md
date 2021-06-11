# Cisco Packet Tracer 

This is where you can build a network in packet tracer with a network simulator. The idea is that whenever you have a huge and complicated network and you want to test the deisgn to check whether it is correct or not and you want to test the IP addresses for example, it is easier to do this on a simulator to check that the network and design is working properly before doing it on the machine and server. 

A switch is in the data link layer which means it does not understand IP addresses but understands MAC addresses.

When a switch doesn't know where to send the data, it will send it to everybody. 

`ping` is a tool that relies on a protocol called ICMP (Internet Control Messaging Protocol) - used to find out whether the computer is up and running - it is blocked from outside the network because it is used for hacking (for security precautions) - it is a network layer protocol

ARP (Address Resolution Protocol) - is a protocol that is used to find the MAC address that corresponds to the IP address. ARP broadcasts to the whole network that it needs the MAC address for the IP address. ARP works in broadcast mode. 

ARP can also check whether someone has the same IP address

## Basic simulation configurations notes:

Give IP addresses to each PC:
IP Configuration > Desktop > IPv4 and Subnet Mask 

To check the connectivity between the computers?
- We have a command called ping in command prompt:
- `ping` and then type in the computer IP address you would like to ping
- You should get back a reply if they are connected

If you want to automatically clear the event list:
option > preferences > Miscellaneous > Auto Clear Event List 

### How can you add the MAC address?
If you run ARP, it will give you the MAC address of the PC that it is pinging. You can find it in the OSI model. ICMP will run after it ARP because it's recieved the MAC address so ARP will not run again. 

`arp -a` - you can check the MAC cache using this command.

## What is a router?
Router is a computer has two network cards and has the ability to do the routing (which is a software functionality)

Any computer you have, you can turn it into a computer. 

Router can block the broadcast 

## Adding the router 
Choose 2911 

Open the router and switch on the router

Config > go on the interface >  and connect the gigaethernet > give IP address (you can give it any IP address) > give subnet mask > switch on 

define default gateway on each PC 

Now you can ping from one PC to another on different networks 

## Between two routers
There is a network between two routers - you need to set up an IP for the two routers as well 

## Static Routing 

you add this when you have more than one router 

You need to set up a static routing because the second router is not directly connected to the PC 

So it needs a path 

in config in the router, set up a static routing 


## What is the difference between router and switch?
Switch does not care about which port it is connected to 
All switch ports by default are the same 

To check which ports you are connected to:
Options > Preferences > Always show port labels in logical workspace 



## What is a default gateway?
The first place the traffic will go to if it doesn't know where to go
For a host is where the traffic should be sent if the destination is not on your network
You need to define a default gateway 

The router will know how to send the traffic on the network but it needs an IP address
Don't make your default ip the same as the broadcast domain ip address - make it random so that it will make it more difficult for hackers

## Explanation of the ARP

ARP sends a signal and sees who has got the IP
The router will receive the broadcast request and act like a hos
idea of a switch - if it doesn't know where the request is supposed to go then it sends it to everyone 
send its to everyone in the broadcast domain

PC0 sending a request to PC3.1
PC0 found out that its not on the same network so now it communicates with the router - gets the mac address of the router and router behvaes a host - whenever the device understands IP addresses, it will stop the broadcast. only switches in layer 3 dont understand the broadcast - to commucation with pc3, we had to do 3 broadcasts - the routers communicate to exchange data - it needs the mac address of the router in order to communicate - router will check the the static routing - router 1 recognised the network and send an ARP broadcast 

Many attacks happens on ARP and ICMP 
PCO NEEDS TO KNOW THE MAC ACCDRESS of interface that takes place on router 1 and then router 1 will need know the interface of the MAC address at router 1 and router 1 recognises the network and will need to know the MAC adrress interface at PC1

