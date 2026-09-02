# Lab 02 - DNS Troubleshooting

## Objective

Simulate a DNS configuration failure on Ubuntu Server, troubleshoot the issue, identify the root cause, restore the correct DNS configuration, and verify name resolution.

## Scenario

The Ubuntu server was able to reach external IP addresses, but domain names were no longer resolving.

The goal was to determine whether the problem was related to:

- Network interface configuration
- Default routing
- Internet connectivity
- DNS resolution

## Environment

- **Host OS:** Windows 11
- **Hypervisor:** Oracle VirtualBox
- **Server:** Ubuntu Server 26.04.1 LTS
- **Network Mode:** NAT
- **Interface:** enp0s3
- **IPv4 Address:** 10.0.2.15

---

## Baseline Validation

Before introducing the failure, I verified that networking and DNS were functioning normally.

Commands used:

`ip -br addr`

`ip route`

`ping -c 4 8.8.8.8`

`ping -c 4 google.com`

`resolvectl status`

Both external IP connectivity and hostname resolution were working.

---

## Simulated Failure

I intentionally configured an invalid DNS server on the Ubuntu network interface:

`sudo resolvectl dns enp0s3 192.0.2.1`

I then verified the new DNS configuration:

`resolvectl status`

The system showed:

`192.0.2.1`

as the configured DNS server.

---

## Troubleshooting

I first tested connectivity to an external IP address:

`ping -c 4 8.8.8.8`

The ping succeeded.

This confirmed that:

- The network interface was working
- The server had an IP address
- The default route was working
- External IP connectivity was available

I then tested hostname resolution:

`ping -c 4 google.com`

The command failed with:

`Temporary failure in name resolution`

Because direct IP connectivity worked while hostname resolution failed, I narrowed the problem down to DNS.

I checked the current DNS configuration using:

`resolvectl status`

The server was using the intentionally incorrect DNS address.

---

## Root Cause

The root cause was an invalid DNS server configured on interface `enp0s3`.

The server still had working network connectivity, but it could not translate domain names into IP addresses.

---

## Resolution

I restored the interface's original DNS settings using:

`sudo resolvectl revert enp0s3`

I verified the configuration again:

`resolvectl status`

The normal DNS servers returned.

---

## Verification

I tested hostname resolution again:

`ping -c 4 google.com`

The domain successfully resolved and responded.

This confirmed that DNS functionality had been restored.

---

## What I Learned

This lab reinforced the difference between IP connectivity and DNS resolution.

A system can have:

- A valid IP address
- A working default gateway
- Internet connectivity

while still being unable to access resources by hostname because DNS is broken.

The troubleshooting process I used was:

**Verify IP configuration → Verify route → Test external IP → Test hostname → Inspect DNS → Identify root cause → Restore DNS → Retest**

This process helped me isolate the problem instead of assuming that all internet connectivity was down.

---

## Screenshots

### Baseline Network Working

![Baseline Network Working](../screenshots/lab2/baseline-network-working.png)

Before introducing the failure, IP connectivity and DNS resolution were functioning normally.

### DNS Failure

![DNS Failure](../screenshots/lab2/dns-failure.png)

External IP connectivity remained available, but hostname resolution failed after configuring the invalid DNS server.

### DNS Restored

![DNS Restored](../screenshots/lab2/dns-restored.png)

After reverting the DNS configuration, hostname resolution worked again.