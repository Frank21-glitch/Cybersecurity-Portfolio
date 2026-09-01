# Cybersecurity Home Lab

## Project Status

🚧 **In Progress**

## Objective

The goal of this project is to build a virtual cybersecurity home lab that simulates a small real-world IT environment.

I will use this environment to develop hands-on skills in:

- Networking
- Windows administration
- Linux administration
- TCP/IP troubleshooting
- DNS
- Firewalls
- SSH
- Security monitoring
- Log analysis
- Incident investigation

Rather than only following tutorials, I will intentionally create, troubleshoot, and document problems inside the lab.

---

## Host System

- **Operating System:** Windows 11
- **CPU:** AMD Ryzen 7 7700X
- **RAM:** 32 GB
- **Storage:** 1 TB

---

## Initial Lab Environment

The first version of the lab will contain the following systems:

### Ubuntu Server

**Purpose:**

- Linux administration
- Networking
- SSH
- Services
- Logging
- Security monitoring

**Resources:**

- 2 CPU cores
- 4 GB RAM
- 40 GB storage

### Windows Client

**Purpose:**

- Windows administration
- Networking
- PowerShell
- Event logging
- Endpoint security

**Planned Resources:**

- 2 CPU cores
- 6 GB RAM
- 64 GB storage

---

## Planned Lab Architecture

```text
Windows 11 Host
 Ubuntu Server
 Linux administration
 SSH
Logging
 Security monitoring

Windows Client
poweshell
Event logging
Endpoint security

The environment will expand later to include:

Windows Server
Active Directory
SIEM monitoring
Additional security systems
Project Methodology

Each lab will follow this process:

Build → Configure → Test → Troubleshoot → Fix → Document

The goal is to understand not only how to configure systems, but also how to investigate and resolve real-world problems.

Current Progress
 Configure virtualization platform
 Deploy Ubuntu Server
 Verify Ubuntu networking
 Configure SSH
 Verify remote SSH access from Windows
 Deploy Windows client
 Configure isolated virtual network
 Test Windows-to-Linux communication
 Create first troubleshooting scenario
 Capture and analyze traffic with Wireshark
 Add security monitoring
Labs
Lab 01 — Ubuntu Server Deployment and Network Validation

Completed:

Deployed Ubuntu Server in VirtualBox
Verified hostname and interface configuration
Verified DHCP addressing and default routing
Confirmed internet connectivity
Confirmed DNS resolution
Verified SSH service availability
Connected remotely from Windows PowerShell

View Lab 01

Ethics

All cybersecurity testing documented in this project is performed only on systems I own, intentionally vulnerable systems, or environments where I have explicit authorization to test.