Cyber Security Task-1
Home Lab Setup: Kali Linux & Metasploitable 2 (Internal Network Configuration)

This repository documents the setup of a secure, isolated penetration-testing environment using VirtualBox, Kali Linux, and Metasploitable 2.
The objective of Task-1 is to create a functional cybersecurity home lab that allows safe experimentation and learning without exposing real systems to risk.

1. Objective
To configure a fully isolated attacker–victim environment by:
Installing Kali Linux (Attacker VM)
Installing Metasploitable 2 (Victim VM)
Connecting both machines through VirtualBox Internal Network
Assigning IP addresses
Testing communication using basic networking commands

2. Tools & Technologies Used
Component	Description
VirtualBox	Virtualization platform for running isolated virtual machines
Kali Linux	Penetration-testing operating system (Attacker)
Metasploitable 2	Intentionally vulnerable Linux OS (Victim)
Internal Network	VirtualBox network mode used to isolate lab from internet & host OS
Linux Networking Commands	ip addr, ifconfig, ping, netstat

3. Network Configuration
Both VMs are placed on an isolated Internal Network named labnet.
Static IPs were assigned for stable communication.

Kali Linux (Attacker)
IP Address: 192.168.100.10/24
Interface: eth0
Network Mode: Internal Network (labnet)

Metasploitable 2 (Victim)
IP Address: 192.168.100.20
Interface: eth0
Network Mode: Internal Network (labnet)

4. Verification of Network Connectivity
Connectivity was validated by sending ICMP echo requests from Kali to Metasploitable.

Ping Test (From Kali → MSF2)
ping -c 4 192.168.100.20

Result
All packets received successfully
0% packet loss
Communication between attacker and victim confirmed

5. Evidence & Screenshots
The repository includes the following screenshots:
Kali ip addr output
Metasploitable ifconfig output
Ping test results
VirtualBox Network Adapter configuration

Proof of successful connectivity
