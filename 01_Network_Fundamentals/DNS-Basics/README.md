# DNS Tools Lab: dig, dig +short, nslookup

## Goal
Practice using DNS lookup tools (`dig`, `dig +short`, `nslookup`) to understand how domain names resolve to IP addresses. Document results with screenshots for my portfolio.

---

## Commands Used

### 1. `dig`
- **What it does:** Performs a DNS lookup for a domain and shows detailed results (query, answer, authority, additional records).
- **Why it matters:** Useful for troubleshooting DNS issues and verifying correct DNS configuration.

**Example I ran:**
```bash
dig google.com
```

**Screenshot:**
![dig_output](dig_google.png)

---

### 2. `dig +short`
- **What it does:** A shorter version of dig that only shows the IP addresses (no detailed records).
- **Why it matters:** Great for quick lookups when you just want the IP.

**Example I ran:**
```bash
dig +short google.com
```

**Screenshot:**
![dig_short_output](dig_short_google.png)

---

### 3. `nslookup`
- **What it does:** Queries DNS to resolve a domain to an IP address (or vice versa).
- **Why it matters:** Common legacy tool still widely used for quick DNS testing.

**Example I ran:**
```bash
nslookup google.com
```

**Screenshot:**
![nslookup_output](nslookup_google.png)

---

## What I Learned
- `dig` shows full DNS records, including the query time and which server responded.
- `dig +short` gives only the IP address — faster for quick lookups.
- `nslookup` works similarly but is older; still common in Windows environments.

---

## Why It Matters in Cybersecurity
- Attackers often use DNS misconfigurations; analysts use these tools to validate DNS integrity.
- Helps detect issues like DNS hijacking, poisoning, or misrouted traffic.
- Quick DNS checks are part of real SOC workflows when investigating suspicious domains.
