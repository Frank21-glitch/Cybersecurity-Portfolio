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
