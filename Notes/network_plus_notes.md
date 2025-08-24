# OSI Model                                                                                                                              8/21/25

### What is the OSI Model?
- Open Systems Interconnection Reference Model

### It's a guide, hence the name model
- Don't get wrapped up in the details

### This is not the OSI Protocol suite
- Most of the OSI protocols didn't catch on

### There are unique protocols at every layer

### You'll refer to this model for the rest of your career
- Often

### All People Seem To Need Data Processing
- Every word's first letter represents the layers

---

# Layer 1 - Physical Layer

### The physics of the network
- Signaling, cabling, connectors
- This layer isn't about protocols

### "You have a physical layer problem."
- Fix your cabling, punch-downs, etc.
- Run loopback test, test/replace cables, swap adapter cards

---

# Layer 2 - Data Link Layer

### The basic network "language"
- The foundation of communication at the data link layer

## Data Link Control (DLC) protocols
- MAC (Media Access Control) address on Ethernet.

## The "switching" layer

---

# Layer 3 - Network Layer

### The "routing" layer

### Internet Protocol (IP)

### Fragments frames to traverse different networks

---

# Layer 4 - Transport Layer

### The "post office" layer
- Parcels and letters
- TCP (Transmission Control Protocol) and UDP (User Datagram Protocol)

---

# Layer 5 - Session Layer

### Communication management between devices
- Start, stop, restart

### Control protocols, tunneling protocols

---

# Layer 6 - Presentation Layer

### Character encoding

### Application encryption

### Often combined with the Application Layer

---

# Layer 7 - Application Layer

### The layer we see
### HTTP, FTP, DNS, POP3

---

# Real-World to OSI model

### Layer 7 - Application Layer
- Your eyes
- Application: https://mail.google.com

### Layer 6 - Presentation Layer
- Application encryption (SSL/TLS)
- Presentation: SSL encryption

### Layer 5 - Session Layer
- Control protocols, tonneling protocols
- Session: Link the presentation to the transport

### Layer 4 - Transport Layer
-  TCP segment, UDP datagram
-  Transport: TCP encapsulation

### Layer 3 - Network Layer
- IP Address, router, packet
- Network: IP encapsulation

### Layer 2 - Data Link Layer
- Frame, MAC address, Extended Unique Identifier ( EUI-48, EUI-64), Switch
- Data Link: Ethernet

### Layer 1 - Physical Layer
- Cables, fiber, and the signal itself
- Physical: Electrical signals

---

# Networking Devices                                                                                                                     8/22/25

### Many different ways to forward traffic
- A data center full of equipment

### Every device has a purpose
- The implementation may change over time
- Once installed, it can often be difficult to remove

### There are new technologies
- Always something to learn

---

# Router

### Routes traffic between IP subnets
-  OSI layer 3 device
-  Routers inside of switches are sometimes called "layer 3 switches"
-  layer 2 = Switch, Layer 3 = Router

### Often connects diverse network types
-LAN, WAN, Copper, Fiber

---

# Switch

### Bridging done in hardware
- Application-specific integrated circuit (ASIC)

### An OSI layer 2 device
- Forwards traffic based on data link address

### Many ports and features
- The core of an enterprise network
- May provide Power over Ethernet (PoE)

### Multilayer switch
- Includes Layer 3 (routing) functionality

---

# Firewalls

### Filter traffic by port number or application
- Traditional vs. NGFW

### Encrypt traffic
- VPN between sites

### Most firewalls can be layer 3 devices (routers)
- Often sits on the ingress/egress of the network
- Network Address Translation (NAT)
- Dynamic routing

---

# IDS and IPS

### Intrusion Detection Systems / Intrusion Prevention System
- Watch network traffic

### Intrustions
- Exploits against operating systems, applications, etc.
- Buffer overflows, cross-site scripting, and other vulnerabilities

### Detection vs. Prevention
- Detection - Alarm or alert
- Prevention - Stop it before it gets into the network

---

# Balancing the load

### Distribute the load
- Multiple servers
- Invisible to the end-user

### Large-scale implementations
- Web server farms, database farms

### Fault tolerance
- Server outages have no effect
- Very fast convergence

---

# Load balancer

### Configurable load
- Manage across servers

### TCP offload
- Protocol overhead

### SSL offload
- Encryption/ Decryption

### Caching
- Fast response

### Prioritzation
- QoS

### Content switching
- Application-centric balancing

---

# Proxies

- Sits between the user and the external network
- Receives the user request and sends the request on their behalf (the proxy)
- Useful fr caching information, access control, URL filtering, and content scanning
- Application may need to know how to use the proxy (explicit)
- Some procies are invisible (transparent)

---

# NAS vs. SAN

### Network Attached Storage (NAS)
- Connect to a shared storage device across the network
- File-level access

### Storage Area Network (SAN)
- Looks and feels like a local storage device
  - Block-level access
- Very efficient reading and writing

### Requires a lot of bandwidth
- May use an isolated network and high-speed network technologies

---

# Access Point (AP)

### Not a wireless router
- A wireless router is a router and an access point in a single device

### An access point is a bridge
- Extends the wired network onto the wireless network
- OSI Layer 2 device

---

# Wireless networks everywhere

### Wireless networking is pervasive
- And you probably don't just have a single access point

### Your access points may not even be in the same building
- One (or more) at every remote site

### Configuration may change at any moment
- Access policy, security policies, AP configs

### The network should be invisible to your users
- Seamless network access, regardless of role

---

# Wireless LAN controllers

### Centralized management of access point
- A single "plane of glass"

### Deploy new access points

### Performance and security monitoring

### Configure and deploy changes to all sites

### Report on access point use

### Usually, a proprietary system
- The wireless controller is paired with the access points

---

# Networking Functions

### a lot is happening behind the scenes
- Many networking functions are part of the infrastructure

### Access to important data
- From anywhere in the world

### Remote access
- Secure network communication

### Traffic management
- Prioritize the important applications

### Protocol support
- Maintain uptime and availability

---

# Content Delivering Network (CDN)

### It takes time to get data from one place to another
- Speeds up the process

### Geographically distributed caching servers
- Duplicate the data
- The user gets the data from a local server

### You're using a CDN server
- Used on many websites
- invisible to the end user

---

# Virtual Private Network (VPN)

### Secure private data traversing a public network
- Encrypted communication on an insecure medium

### Concentrato / head-end
- Encryption/decryption access device
- Often integrated into a firewall

### Many deployment options
- Specialized cryptographic hardware
- software-based options available

### Often used with client software
- Sometimes built into the OS

---

# Quality of Service (QoS)

- Traffic shaping, packet shaping
- Control by bandwidth usage or data rates
- Set important applications to have higher priorities than other apps

### Manage the QoS 
- Routers, switches, firewalls, QoS devices

---

# Time to Live (TTL)

### How long should data be available
- not all systems or protocols are self-regulating
- we sometimes need to tell a system when to stop

### Create a timer
- Wait until a number of hops, or wait until a certain amount of time elapses
- then stop (or drop)

### Many different uses
- drop a packet caught in a loop
- clear a cache

---

# Routing loops

### Router A thinks the next hop is to router B
- Router B thinks the next hop is Router A
- And repeat

### Easy to misconfigure
- Especially with static routing

### This can't go on forever
-TTL is used to stop the loop

---

# IP (Internet Protocol)

### Loops could cause a packet to live forever
- Drops the packer after a certain number of hops

### Each pass through a router is a hop
- Default TTL for macOs/linux is 64 hops
- Default TTL for Windows is 128 hops

 ### The router decreases TTL by 1
 - A TTL of sero is dropped by the router

---

# DNS (Domain Name System)

### DNS lookups
- Resolve an IP address from a fully-qualified domain name
- https://www.google.com = 172.253.122.101

### A device caches the lookup for a certain amount of time
- How long? TTL seconds long.

---

# Designing the cloud

### On-demand computing power
- Click a button

### Elasticity
- Scale up or down as needed

### Application also scale
- Scalability for large implementations
- Access from anywhere

### Multitenancy
- Many different clients are using the same cloud infrastructure

---

# Virtual Networks

### Server farm with 100 individual computers
-it's a big farm

### All servers are connected with enterprise switches and routers
- With redundancy

### Migrate 100 physical servers to one physical server
- With 100 virtual servers inside

### What happens to the network?

---

# Network function virutalization (NFV)

### Replace physical network devices with vitrual versions
- manage from the hypervisor

### Same functionality as a physcial device
- Routing, switching, load balancing, firewalls, etc

### Quickly and eaily depploy network functions
- Click and deploy from hypervisor

### Many different deployment options
- Virtual machine, container, fault tolerance, etc

---

# Connecting to the cloud

### Virtual Private Cloud (VPC)
- A pool of resources created in a public cloud

### Common to create many VPCs
- Many different application clouds

### Connect VPCs with a transit gateway
- And users to VPCs
- A "cloud router"

### Now make it secure
- VPCs are commonly on different IP subnet
- Connecting to the cloud is often through a VPN

---

### VPN (Virtual Private Network)
- Site-to-site VPN through the internet

### Virtual Private Cloud Gateway / Internet gateway
- Connects users on the internet

### VPN NAT gateway
- Network address translation
- Private cloud subnets connect to external resources
- External resources cannot access the private cloud

### VPC endpoint 
- Direct connection between cloud provider networks

---

# Security groups and list

### A firewall for the cloud
- control inbound and outbound traffic flows

### Layer 4 port number
- TCP or UDP port

### Layer 3 address
- Individual addresses
- CIDR block notation
- IPv4 or IPv6

---

# Network security list

### Assign a security rule to an entire IP subnet
- Applies to all devices in the subnet

### Very Broad
- Can become difficult to manage
- not all devices in a subnet have the same secuitry posture

### More granularity may be needed
- Broad rules may not provide the right level of security

---

# Network security group

### Assign a security rule to a specific virtual NIC (VNIC)
- Applies to specific devices and network connections

### More granular than network security lists
- Different rules for devices in the same IP subnet

### Better control and granularity
- The best practice for cloud and security rules

---

# Cloud deployment models

### Public
- Available to everyone over the internet

### Private
- Your own virtualized local data center

### Hybrid
- A mix of both

---

# Software as a Service (SaaS)

### On-demand software
- No local installation
- Why manage your own email distribution or payroll?

### Central management of data and application
- Your data is out there

### A complete application offering
- No development work required
- Google mail, office 365

---

# Infrastructure as a Service (IaaS)

### Sometimes called Hardware as a Service (HaaS)
- Outsource your equipment

### You're still responsible for the management
- and for the security

- Your data is out there, but more within your control

- Web server providers

---

# Platform as a Service (PaaS)

### No servers, no software, no maintenance team, no HVAC
- Someone else handles the platform, you handle the development

### You don't have direct control of the data, people, or infrastructure
- Trained security professionals are watching your stuff
- Choose carefully

### Put the building blocks together
- Develop your app from what's available on the platform
- SalesForce.com

---

# Introduction to IP  8/23/25

## A series of moving vans

### Efficiently move a large amount of data
- Analogy: Moving a truck to get data from one house to another

### The network topology is the road
- Ethernet, DSL, cable system

### The truck is the Internet Protocol (IP)
- We've designed the roads for this truck

### The boxes hold your data
- Boxes of TCP and UDP

### Inside the boxes are more things
- Application information

---

# TCP and UDP

### Transported inside of IP
- Encapsulated by the IP protocol

### Two ways to move data from place to place
- Different features for different applications

### OSI Layer 4
- The transport layer

### Multiplexing
- Use many different applications at the same time
- TCP and UDP

---

# TCP - Transmission Control Protocol

### Connection-oriented
- A formal connection setup and close

### "Reliable" Delivery
- Recovery from errors
- can manage out-of-order messages or retransmission

### Flow control
- The receiver can manage how much data is sent

---

# UDP - User Datagram Protocol

### Connectionless
- No formal open or close to the connection

### "Unreliable" delivery
- No error recovery
- No reordering of data or retransmission

### No flow control
- The sender determines the amount of data transmitted

---

# Speed Delivery

### The IP delivery truck delivers from one (IP) address to another (IP) address
- Every house has an address, every computer has an IP address

### Boxes arrive at the house / IP address
- Where do the boxes go
- Each box has a room name

### Port is written on the outside of the box
- Drop the box into the right room

---

# Lots of ports

### IPv4 sockets
- Server IP address, protocol, server application port number
- Client IP address, protocol, client port number

### Non-ephemeral ports permanent port numbers
- Ports 0 through 1,023
- Usually on a server or service

### Epherman ports - temporary port numbers
- Ports 1,024 through 65,535

---

# Port numbers

- TCP and UDP ports can be any number between 0 and 65,535

### Most servers (services) use non-ephemeral (not temporary) port numbers
- This isn't always the case
- it's just a number

### Port numbers are for communication, not security

### Service port number needs to be "well-known"

### TCP port numbers aren't the same as UDP port numbers

---

# Ports on the network

### Web server - tcp/80

### VoIP server - udp/5004

### Email server - tcp/143

---






