# Cybersecurity Portfolio

Welcome to my cybersecurity portfolio.

I am a cybersecurity student building hands-on experience in networking, Linux, Windows administration, troubleshooting, security monitoring, and incident investigation.

I currently hold the **CompTIA Network+ (N10-009)** certification and am working toward an **A.A.S. in Cybersecurity**.

My goal with this portfolio is to go beyond coursework and document practical labs where I configure systems, create problems, troubleshoot them, identify root causes, and verify solutions.

---

## Current Skills

- TCP/IP networking
- DNS and DHCP
- Network troubleshooting
- Linux administration
- SSH
- Linux firewall management with UFW
- VirtualBox
- Windows administration
- PowerShell
- Wireshark
- Nmap
- Git and GitHub
- Python fundamentals

---

# Projects

## 01 - Cybersecurity Home Lab

A virtualized home lab designed to simulate real-world IT and cybersecurity troubleshooting scenarios.

### Completed Labs

- **Lab 01 - Ubuntu Server Deployment and Network Validation**
  - Deployed Ubuntu Server in VirtualBox
  - Verified IP addressing and routing
  - Tested internet connectivity and DNS
  - Configured and verified SSH
  - Connected remotely from Windows PowerShell

- **Lab 02 - DNS Troubleshooting**
  - Simulated a DNS configuration failure
  - Verified that IP connectivity still worked
  - Identified DNS as the root cause
  - Restored DNS configuration
  - Verified successful name resolution

- **Lab 03 - SSH Firewall Troubleshooting**
  - Simulated an SSH outage using UFW
  - Verified that SSH remained active
  - Confirmed TCP port 22 was listening
  - Identified the firewall as the root cause
  - Restored remote SSH connectivity

## Lab 01 — Ubuntu Server Deployment

I deployed my first Ubuntu Server VM and worked through the basic setup.

I verified the hostname, IP address, routing, internet access, DNS, and SSH.

I also tested logging into the server remotely from Windows.

[View Lab 01](./labs/lab-01-ubuntu-server-deployment.md)

---

## Lab 02 — DNS Troubleshooting

In this lab, I intentionally broke DNS on the Ubuntu server while keeping the network connection working.

This helped me understand the difference between having network connectivity and actually being able to resolve domain names.

I used tools like `ping` and `resolvectl` to find the problem and restore DNS.

[View Lab 02](./labs/lab-02-dns-troubleshooting.md)

---

## Lab 03 — SSH and Firewall Troubleshooting

I created an SSH connection problem by changing firewall rules on the Ubuntu server.

I checked whether SSH was running, verified the listening port, inspected the firewall, found the cause of the connection failure, and restored access.

[View Lab 03](./labs/lab-03-ssh-firewall-troubleshooting.md)

---

## Lab 04 — Linux Users, Groups, and Permissions

I created a protected directory and used Linux users, groups, ownership, and permissions to control access.

I then removed a user from the required group to create a real `Permission denied` problem.

I investigated the issue and restored the correct group membership.

[View Lab 04](./labs/lab-04-linux-permissions-troubleshooting.md)

---

## Lab 05 — Windows 11 Client Deployment

I deployed a Windows 11 Pro VM and started learning Windows administration through PowerShell.

I worked with:

- Local users
- Local groups
- Administrator membership
- Windows services
- Microsoft Defender
- Processes
- TCP connections
- Windows Event Logs
- Networking and DNS

[View Lab 05](./labs/lab-05-windows-client-deployment.md)

---

## Lab 06 — Windows Server 2025 Deployment

I deployed Windows Server 2025 and configured it as `DC01`.

Before installing Active Directory, I learned how to use Server Manager and PowerShell to inspect the server, networking, services, connections, and event logs.

[View Lab 06](./labs/lab-06-windows-server-deployment.md)

---

## Lab 07 — Active Directory Domain Deployment

This was the point where the lab started becoming a real Windows domain environment.

I configured `DC01` with a static IP address and installed:

- Active Directory Domain Services
- DNS Server
- Group Policy Management

I then promoted `DC01` to a Domain Controller and created my first Active Directory forest:

`franklab.test`

I verified the domain with PowerShell, Active Directory Users and Computers, and DNS Manager.

[View Lab 07](./labs/lab-07-active-directory-domain-deployment.md)

---

## Lab 08 — Active Directory Users, Groups, and OUs

I started organizing the domain like a small company.

I created departments for:

- IT
- HR
- Sales

I created domain accounts:

- `it.user`
- `hr.user`
- `sales.user`

I also created security groups:

- `GG-IT`
- `GG-HR`
- `GG-Sales`

Each user was placed into the correct department and security group.

I verified everything using both Active Directory Users and Computers and PowerShell.

[View Lab 08](./labs/lab-08-active-directory-users-groups-ous.md)

---

## Lab 09 — Windows 11 Domain Join and Authentication

In this lab, I connected `WIN11-CLIENT01` to the `franklab.test` domain.

I configured the client with:

- Static IP: `192.168.50.20`
- DNS Server: `192.168.50.10`

Before joining the domain, I verified that the client could communicate with `DC01` and locate the Active Directory DNS and LDAP records.

I then joined the workstation to the domain and logged in using:

`FRANKLAB\it.user`

I also verified that:

- `DC01` was the logon server
- `WIN11-CLIENT01` appeared in Active Directory
- The workstation was part of `franklab.test`
- Group Policy information was being received from the domain

[View Lab 09](./labs/lab-09-domain-join-and-authentication.md)

---

# Current Active Directory Structure

```text
franklab.test
|
├── Domain Controllers
│   └── DC01
|
├── Computers
│   └── WIN11-CLIENT01
|
├── Employees
│   ├── IT
│   │   └── IT User
│   ├── HR
│   │   └── HR User
│   └── Sales
│       └── Sales User
|
└── Groups
    ├── GG-IT
    ├── GG-HR
    └── GG-Sales
```
---

### Next Lab

- **Lab 10 — Group Policy Administration.**

[View Cybersecurity Home Lab](./01-Cybersecurity-Home-Lab/)

---

## Upcoming Projects

### Windows and Active Directory Lab

Planned topics:

- Windows 11 client deployment
- Windows Server
- Active Directory Domain Services
- Domain Controllers
- Users and security groups
- Organizational Units
- Group Policy
- DNS in Active Directory
- Domain joins
- Authentication troubleshooting
- Windows Event Logs

### Network Traffic Analysis

Planned topics:

- Wireshark
- TCP handshakes
- DNS traffic
- ICMP
- HTTP/HTTPS
- SSH traffic
- Packet filtering
- Network troubleshooting

### SOC / SIEM Lab

Planned topics:

- Centralized logging
- Windows security events
- Linux logs
- Authentication monitoring
- Alert investigation
- Incident documentation
- SIEM technologies

### Security Automation

Planned topics:

- Python
- Log parsing
- Failed login detection
- Basic security automation
- Report generation

---

# Certifications

- **CompTIA Network+ (N10-009)**

---

# Education

- **Wakefield High School Diploma**


- **A.A.S. in Cybersecurity - In Progress**

---

# Lab Methodology

My labs follow a structured troubleshooting process:

**Build → Configure → Test → Break → Investigate → Fix → Verify → Document**

For each troubleshooting lab, I document:

1. Objective
2. Scenario
3. Environment
4. Baseline
5. Simulated failure
6. Troubleshooting process
7. Root cause
8. Resolution
9. Verification
10. Lessons learned
11. Screenshots

---

# Portfolio Goals

I am building this portfolio to develop practical experience in:

- IT support and troubleshooting
- Network administration
- Windows and Linux administration
- Active Directory
- Security operations
- Log analysis
- Incident response
- Vulnerability management
- Security automation

---

# Ethics

All cybersecurity testing documented in this portfolio is performed only on systems I own, intentionally vulnerable systems, or environments where I have explicit authorization to test.
