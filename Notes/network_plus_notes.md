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
