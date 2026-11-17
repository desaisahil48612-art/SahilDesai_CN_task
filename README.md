Multinational Company Network Design
A computer network simulation for a multinational company, built in Cisco Packet Tracer. The design uses a suitable network topology with classless IP addressing (CIDR/VLSM), a multi-service server, 50 computers, and 3 layers of security.
Project Overview
Item
Details
Project
Network design and simulation for a multinational company
Tool
Cisco Packet Tracer
Topology
Star / Hierarchical (core, distribution, access)
IP Addressing
Classless (CIDR / VLSM)
End Devices
50 computers
Security
3 layers
Objectives
Design a scalable, reliable network for a multinational company.
Use classless IP addressing to avoid wasting addresses.
Configure one server to provide DHCP, HTTP, DNS, Email and FTP.
Connect 50 computers and verify end-to-end connectivity.
Apply 3 layers of security to protect the network.
Network Topology
Core layer: high-speed router(s) connecting the sites/branches.
Distribution layer: routers/layer 3 switches for routing and policy.
Access layer: switches connecting the 50 computers.
Server farm: one server hosting all network services.
Add a screenshot of your topology here: ![Topology](topology.png)
IP Addressing Scheme (Classless)
Example plan using VLSM (replace with your actual values):
Network / Department
Hosts
Network Address
Subnet Mask
Usable Range
LAN 1
25
192.168.1.0
/27 (255.255.255.224)
192.168.1.1 - 192.168.1.30
LAN 2
25
192.168.1.32
/27 (255.255.255.224)
192.168.1.33 - 192.168.1.62
Server Network
5
192.168.1.64
/29 (255.255.255.248)
192.168.1.65 - 192.168.1.70
Router Links
2
192.168.1.72
/30 (255.255.255.252)
192.168.1.73 - 192.168.1.74
Server Services
Service
Purpose
DHCP
Automatically assigns IP addresses to the 50 computers
DNS
Resolves domain names (e.g., www.company.com) to IP addresses
HTTP
Hosts the company web page
Email
Internal email (SMTP/POP3) between users
FTP
File upload and download between users and the server
Security (3 Layers)
Physical / Device Security: console and VTY passwords, encrypted enable password (enable secret), SSH instead of Telnet.
Network Security: Access Control Lists (ACLs) and firewall rules to allow only required traffic to the server.
Access / Port Security: switch port security, unused ports shut down, VLAN segmentation.
How to Run the Simulation
Install Cisco Packet Tracer.
Download the .pkt file from this repository.
Open it in Packet Tracer.
Check that PCs get IP addresses automatically via DHCP.
Test services from any PC:
HTTP: open the Web Browser and visit the server IP or domain name.
DNS: use the domain name instead of the IP address.
Email: configure the Email app and send a mail between two PCs.
FTP: run ftp <server-ip> from the command prompt.
Use ping to verify connectivity between networks.
Repository Contents
sahil_CN_task/
├── README.md
├── Network_Design.pdf      # Network design documentation
└── <your_simulation>.pkt   # Packet Tracer simulation file
Author
Sahil Desai GitHub: desaisahil48612-art
