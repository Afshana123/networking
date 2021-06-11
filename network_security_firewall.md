# What is a firewall?
A layer 3 device but it can also be a system or a software 
A system or a group of systems which enforces an access control policy between networks 

All firewalls share some common properties:
- resistant to network attacks - they can filter traffics - they can allow or deny access based on the rules they have or based on ACL 
- they enforce this access list
- can either be a software or a hardware
- if software, they can install on a host or a server etc 
- if hardware, this is just like another computer which can enforce ACL or a policy 

By default, when you install a firewall it will:
- your network will be allowed to access any external network
- external network will not be allowed to access internal networks

# How the firewall enforces a policy 

## Access control list (ACL) 
- contains the rules that grant or deny access to certain resources 
- any ACL is a set of rules to either grant or deny access to a resource
- When we write a policy for a firewall, we write a ACL 
- ACL filters access to the network or network resources 
- When we want to protect, limit or grant access to a system, we write an ACL

## Actions for ACL
a list that contains the rules that grants or denies access to a certain resource
e.g it might be a host, file or printer etc 
The actions for ACL is either - firewall policy:
-grant
-deny

## Target of ACL:
to filter access to the network or network resources

An access list for a CISCO firewall is different from a windows firewall. 

## Benefits of a firewall
- to protect your network 
- protect the users from the inside from attacks on the outside 


you place the firewall in the networking model TCP/OSI model

## packet filtering firewall
controls the network access by analysing the outgoing/incoming packets based on the information of the network layer and transport layer.

When a firewall decides to allow or deny a specific packet, it will check the source IP address, the destination IP address, the source port and the destination port and whether it is TCP/UDP. 

Firewall will intercept these packets and checks each field in order to allow or deny access through the access list by checking if there is a match

## Application gateway firewall
checks the application data.  
Whenever you have a firewall, you need to know the capabilities of the firewall and what layer it can work.

# Firewall Zone 
When you have a firewall, you have a firewall zone. In a firewall zone:
- you have the inside/private and trusted zone 
- public and untrusted zone 
- We can add a third zone called DMZ (zone which can be accessed from the outside in order to use certain services e.g web server because you want the user from the internet to access the server but not anything else)
- You would allow access to the outside zone through the DMZ 