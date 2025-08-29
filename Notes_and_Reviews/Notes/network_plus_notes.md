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

###
