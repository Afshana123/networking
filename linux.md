# Networking in Linux 

## Labtainer
Ltainer is a virtual machine lab which is a lab using containers 

Labatainer is a lab based on docker containers, and it will take care of creating these hosts and the networks between them- you don't need to create the container maunally - all we need to do is configure these containers/hosts in the network in order to be able to exhcnage data between them 

Each container represents a host, router or a firewall in the network 

The packet tracer was a graphical configuration, Labtainer is on Linux shell open for each one of these containers/hosts


## How to perform the lab

open linux shell and run:
`cd $LABTAINER_DIR/scripts/labtainer-student`

To see a list of available commands for the labs:
`labtainer`

Linux firewall is called `iptables`

When you perform the lab, it will open all the containers for that lab.

`stoplab` - After you finish, you type this command in the /labtainer-student main linux shell which will destroy all the containers that were created for that specific lab and save the configuration in a zip file. 

To restart the lab from the beginning:
`labtainer -r <labname>`

## Command Lines in Linux 

`ifconfig` - will give you a list of interfaces you have on your computer that are up and running

if `ifconfig` is not installed on the machine:
`sudo apt install net-tools`

"inet" - gives the ip address for the interface

`<netmask>` - is the subnet mask

`<ether>` - gives the MAC address for the interface

lo - Each machine has a loopback interface

127.0.0.0 - your own machine
127.0.0.1 - The first loopback 

`localhost` = `ping 127.0.0.1` - doing a ping to your own machine - you are accessing the same machine that you are working on. You are testing whether the TCP stack is - press Ctrl+C to stop it 

`ifconfig -a` - a list of interface that are working on the machine and the interfaces that are down too 

`route` - list of routing table in this machine

`route -n` - if you want the IP addresses instead of the names 

`arp` - will give us the MAC address - a list of entry that has already been mapped using the arp protocol

`arp -n` - will give the IP addresses instead of the names

install the new package:
`sudo apt install iproute2`

if you want all the ip adresses - `ip address` or `ip add` or `ip a` which means the same thing - you will get a list of all the interfaces 

"inet6" - means IP version 6

If you want to switch off the interface using the new command:
`sudo ip link set enp0s3 down`

"enp0s3" - the interface used to connect to the internet right now

If you want to switch on the interface using the new command:
`sudo ip link enp0s3 up`

Using the old command:
`sudo ifconfig enp0s3 down`

How do see whether it is down:
`ifconfig -a`

To assign an IP address to an interface:
`sudo ip address add 10.0.2.15/255.255.255.0 dev enp0s3`
"dev" means device

or we can assign it like this:
`sudo ip address add 10.0.2.15/24.0 dev enp0s3`

r using the old command:
`sudo ifconfig enp0s3 10.0.2.15 netmask 255.255.255.0`

How to remove an IP address from the interface:
`sudo ip address del 10.0.2.15/24 dev enp0s3`

How to add the default gateway:
`sudo ip route add default via 10.0.2.2`

`ip route` - routing table using the new command 

`./get labs.sh` - the Sparta Global Labs 

## Chaging to UK settings 
`echo "setxkbmap gb" >> -/.profile`- UK keyboard layout

`echo "setxkbmap gb" >> -/.bashrc` 

`sudo timedatectl set-timezone Europe/London` - To set the time-zone

## What is Telnet?
We used SSH to access the server or remote machine, but we added a key and encryption.
SSH is encrypted - it will open a remote shell on your remote machine 
Telnet does the same, but the difference is that it is not encrypted - not recommended to use Telnet

## Overview after doing the Sparta Global labs:

ping - checks the end to end connectivity 

traceroute 
- will check whether for example doing a ping between host 11 and 21 and check whether it will recieve back any connection 
- it will check all the rotuers on the way whether it can connect or not
- it will trace the whole route 

`wget` - to get a file from a web-server


