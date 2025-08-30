### OSI Model = Open System Interconnection Reference Model
- Used in IT to describe the process data takes to traverse the network
- It's a guide
- not describing the OSI protocol suite
- Many different protocols that might operate at each layer of the OSI Model
- Use this for the rest of your career
- All (Application), People (Presentation), Seem (Session), To (Transport), Need (Network), Data (Data Link), Processing (Physical)

---

### Layer 1 - Physical
- Physical signals that we send through the cables and fibers on our network
- No protocols since we are talking about getting a signal from one part of a network to the other
- Example: you have a physical layer problem = fix your cable, test, or replace cables
- Troubleshooting in layer 1 usually involves loopback tests, testing cables and fibers, and swapping adapter cards

---

### Layer 2 - Data Link
- Fundamental layer that is used to communicate between two devices on the network
- referred to as the MAC address later -> Data Link Control (DLC) layer
- commonly used with the network cards on our devices
- Ethernet adapter or wireless refer to that physical address on the device as the DLC address or MAC Address
- MAC = Media Access Control
- the switching layer

--- 

### Layer 3 - Network Layer
- Routing Layer
  - Routers use to determine how to forward traffic
  - Routers specifically looking at the destination IP address
- Fragment frames into multiple pieces to move

---

### Layer 4 - Transport Layer
- Post office layer -> transporting info from one device to another
- TCP (Transmission Control Protocol) and UDP (User Datagram Protocol)
  - Responsible for getting all the info from within our IP packets from one device to another
  - large amount of data -> small piece -> putting it together on the other side

---

### Layer 5 - Session Layer
- Responsible for creating a session so that a device can receive that information
- Communication Management between Point A to Point B
  - Stop or restart or start
- Control protocols, tunelling protocol

---

### Layer 6 - Presentation Layer
- Responsible for putting all of this data into a format that we will see with our eyes
- Character encoding
- Application encryption
- Often combined with the Application Layer

---

### Layer 7 - Application Layer
- The layer we see on our screen
- Common applications that would operate at the OSI Layer 7
  - HTTP, FTP, DNS, POP3
 
---

### Real World to OSI Model
- **Layer 1 - Physical:** Cables, fiber, and the signal itself
- **Layer 2 - Data link:** Frame, MAC address, Extended Unique Identifier (EUI-48, EUI-64), Switch
- **Layer 3 - Network:** IP address, Router, Packer
- **Layer 4 - Transport:** TCP segment, UDP datagram
- **Layer 5 - Session:** Control protocols, tunneling protocols
- **Layer 6 - Presentation:** Application Encryption (SSL/TLS)
- **Layer 7 - Application:** Your eyes

- **Layer 1 - Physical:** Electrical Signals
- **Layer 2 - Data link:** Ethernet
- **Layer 3 - Network:** IP encapsulation
- **Layer 4 - Transport:** TCP Encapsulation
- **Layer 5 - Session:** Link the presentation to the transport
- **Layer 6 - Presentation:** SSL Encryption
- **Layer 7 - Application:** https://mail.google.com

---

### Network Devices
- Different ways to move traffic
  - A data center full of equipment
- Every device has a purpose
- There are new devices or new technology

---

### Router
- takes data from one IP subnet -> route to different IP subnet
  - Referenced in the OSI Layer 3 (Network layer) device
  - sometimes used in layer 2 = switch and layer 3 = router
- Connects many different types of networks
  - EX: LAN, WAN, copper, fiber

---

### Switch
- Switches operate in the MAC address layer (data link layer)
- operates in the hardware of the device
  - Referred to as Application-specific integrated circuit (ASIC)
- OSI layer 2 device
- many functions and ports
  - May provide Power over Ethernet (PoE)
- sometimes referred to as a layer 3 (routing) if the switch includes some type of routing functionality built in the device itself

---

### Firewalls
- allows you to filter traffic through TCP or UDP port number
- Modern firewalls are called Next Generation Firewall (NGFW)
  - able to identify apps traversing the network
  - able to manage if that app should be allowed or not
- firewalls commonly allow us to encrypt traffic traversing the network through a VPN
  - VPN = Virtual Private Network
- Most Firewalls can operate in layer 3 meaning they can act as a router
  - Why? often sits on the ingress/egress of the network
  - also provides Network Address Translation (NAT)
  - dynamic routing
 
---

### IDS and IPS
- Intrusion Detection System / Intrusion Prevention System
- Much of it is integrated with the NGFW
- Known attack types:
  - exploits against the OS and, application you're using
  - buffer overflow, cross-site scripting, and more
- Detection -> alarm or alert
- Prevention -> block it before it gets inside the network. Commonly used

---

### Balancing the Load
- Load balancer -> distribute the load across multiple servers
- Large number of web servers, or database farms
- Load balancers are good at identifying outages to these servers
- Optimise the communication -> TCP offloading
- SSL Offload -> provide the encryption and decryption capabilities
- Caching -> request made to the load balancer, instead of going all the way to the server to provide data
- Prioritization -> higher access = QoS (Quality of Service)
- Content switching -> certain pages might be on certain servers all of request will go on individual servers

---

### Proxies
- Takes user request -> preforming that request on their behalf -> receives answer -> verifies if the answer doesn't contain malicous software or malicous code -> provides answer to end user
- sits in the middle of communication, make communication on user behalf
- perfect place for caching, access control, URL filtering, content scanning
- some applications may need to know how to use the proxy (explicit)
- Some proxies are invisible (tranparent)

---

### NAS vs. SAN
- Network Attached Storage (NAS)
  - Provides file level access
- Storage Area Network (SAN)
  - looks and feels like a local storage device
    - block level
  - an efficient way to change a bit of infor within the large document
- need a lot of bandwidth
  - may use isolated network and high speed network tech
 
---

### Access Point (AP)
- not a wireless router
- allows us to communicate wirelessly from our device to the rest of the network
- bridging communication between wireless netowrk and the wired Ethernet network
  - OSI Layer 2 (data link) device

---

### Wireless Network everywhere
- wireless networking is pervasive, you might have more access points
- access point might not be in the same building
- configuration may change at any moment
- always making sure people can roam from one access point to another so they're always connected

---

### Wireless LAN controller
- Centralized management tool -> allow us manange all of our access point from one central place
  - single plane of glass = allow us to manage the entire infrastructure while we are chilling
- deploy new access point
- performance and security monotoring
- changes to make and deploy them to all sites
- report on access points use
- usually a proprietary system
  - wireless controller is paired with the access point 
