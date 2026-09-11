# Cybersecurity Home Lab

## About This Project

This is my personal cybersecurity home lab where I’m building out a small virtual IT environment and learning by actually working with the systems.

Instead of only watching tutorials, I’ve been setting things up myself, breaking things on purpose, troubleshooting problems, fixing them, and documenting what happened.

The lab started with Linux and networking, then expanded into Windows, Windows Server, Active Directory, DNS, domain authentication, and user management.

My goal is to keep building this environment over time and use it to get more hands-on experience with the tools and concepts used in IT and cybersecurity jobs.

---

## What I'm Practicing

Some of the areas I’m working on include:

- Windows administration
- Windows Server
- Active Directory
- Linux administration
- PowerShell
- Networking
- TCP/IP
- DNS
- SSH
- Firewalls
- Users and groups
- Permissions
- Group Policy
- Windows Event Logs
- Troubleshooting
- Security monitoring
- Log analysis
- Incident investigation

---

## Host System

- **OS:** Windows 11
- **CPU:** AMD Ryzen 7 7700X
- **RAM:** 32 GB
- **Storage:** 1 TB
- **Virtualization:** Oracle VirtualBox

---

## Current Lab Environment

### Ubuntu Server

Used for:

- Linux administration
- Networking
- SSH
- Services
- File permissions
- Troubleshooting

Resources:

- 2 CPU cores
- 4 GB RAM
- 40 GB storage

---

### Windows 11 Client

**Hostname:** `WIN11-CLIENT01`

Used for:

- Windows administration
- PowerShell
- Domain authentication
- Event logs
- Endpoint security
- Group Policy testing

Resources:

- 2 CPU cores
- 6 GB RAM
- 80 GB storage

---

### Windows Server 2025

**Hostname:** `DC01`

Used for:

- Active Directory Domain Services
- DNS
- Domain authentication
- Group Policy
- User and computer management

**Domain:** `franklab.test`

**IP Address:** `192.168.50.10`

---

## Current Active Directory Setup

```text
                 franklab.test
                       |
                      DC01
               Windows Server 2025
                  192.168.50.10
                  AD DS + DNS
                       |
                  AD-LAB-NET
                192.168.50.0/24
                       |
                WIN11-CLIENT01
                  192.168.50.20
                       |
                FRANKLAB\it.user
```

---

# Labs

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

# Progress

- [x] Ubuntu Server deployment
- [x] Linux networking
- [x] DNS troubleshooting
- [x] SSH setup
- [x] Firewall troubleshooting
- [x] Linux users and groups
- [x] Linux permissions troubleshooting
- [x] Windows 11 deployment
- [x] PowerShell basics
- [x] Windows Event Logs
- [x] Windows Server 2025 deployment
- [x] Active Directory installation
- [x] DNS Server setup
- [x] Domain Controller promotion
- [x] Active Directory forest creation
- [x] Organizational Units
- [x] Domain users
- [x] Security groups
- [x] Group membership
- [x] Windows domain join
- [x] Domain user login
- [x] Domain computer verification
- [ ] Group Policy
- [ ] Shared folders and NTFS permissions
- [ ] Account lockout troubleshooting
- [ ] Failed login investigation
- [ ] Windows security auditing
- [ ] Wireshark traffic analysis
- [ ] Sysmon
- [ ] SIEM
- [ ] Security monitoring
- [ ] Incident investigation

---

## How I'm Building the Lab

The way I’ve been approaching each lab is:

**Build → Test → Break → Troubleshoot → Fix → Verify → Document**

I’m trying to understand what is actually happening instead of just getting to the point where something works.

When I run into errors, I document those too because troubleshooting has been one of the most useful parts of building the lab.

---

## What's Next

I plan to keep expanding the environment with:

- Group Policy
- Shared folders
- NTFS permissions
- Account lockout troubleshooting
- Windows Security logs
- Authentication auditing
- Wireshark
- Sysmon
- SIEM monitoring
- Detection and alerting
- Incident response scenarios

---

## Ethics

Everything in this project is done inside systems I own or lab environments I created for learning.

Any security testing is performed only in environments where I have permission to do so.