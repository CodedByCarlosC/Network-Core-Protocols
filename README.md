# 🌐 Networking Core Protocols – Hands-On Lab

## 📘 Overview

This repository documents my hands-on learning of **core networking protocols** through a TryHackMe lab environment.

The focus of this project was to understand how common internet services operate **behind graphical interfaces**, by examining how protocols communicate, authenticate, and exchange data at the application layer.

These protocols form the foundation of web traffic, file transfers, and email communication—making them critical knowledge for cybersecurity, networking, and system administration roles.

---

## 🧠 Protocols Covered

### 🔹 Domain Name System (DNS)
- Resolves domain names to IP addresses
- Explored common record types:
  - A, AAAA
  - CNAME
  - MX
- Reviewed DNS behavior over UDP/TCP port 53
- Used `nslookup` to examine DNS queries and responses

![image alt](https://github.com/CodedByCarlosC/Network-Core-Protocols/blob/5e4cb2df8454b94f90e203b0d906d6019a02dac8/dnssec%20me.PNG)
![image alt](https://github.com/CodedByCarlosC/Network-Core-Protocols/blob/5e4cb2df8454b94f90e203b0d906d6019a02dac8/dnssec%20signed.PNG)

Beyond the lab exercises, I applied this knowledge to my own deployed portfolio website by:

- Reviewing and updating my domain's DNS configuration
- Verifying DNS propagation
- Inspecting DNSSEC status
- Validating A and CNAME records for proper resolution

This practical application reinforced how DNS configuration directly impacts website availability, trust, and security.

![image alt](https://github.com/CodedByCarlosC/Network-Core-Protocols/blob/5e4cb2df8454b94f90e203b0d906d6019a02dac8/nslookup.PNG)

---

### 🔹 WHOIS
- Examined domain registration data
- Identified registrant, registrar, and record timestamps
- Discussed privacy protection services and their impact
- Used WHOIS as an OSINT-style information source

![image ult](https://github.com/CodedByCarlosC/Network-Core-Protocols/blob/5e4cb2df8454b94f90e203b0d906d6019a02dac8/whois%20me.PNG)

---

### 🔹 HTTP & HTTPS
- Studied how browsers communicate with web servers
- Reviewed common HTTP methods:
  - GET, POST, PUT, DELETE
- Examined HTTP traffic using Wireshark
- Manually interacted with web servers using `telnet`
- Reviewed default ports:
  - HTTP: 80
  - HTTPS: 443

---

### 🔹 File Transfer Protocol (FTP)
- Focused on efficient file transfers
- Reviewed core FTP commands:
  - USER, PASS
  - LIST, RETR, STOR
- Observed separate control and data connections
- Analyzed FTP traffic using Wireshark
- Default port: TCP 21

![image alt](https://github.com/CodedByCarlosC/Network-Core-Protocols/blob/5e4cb2df8454b94f90e203b0d906d6019a02dac8/ftp%20file%20transfer.PNG)

---

### 🔹 Simple Mail Transfer Protocol (SMTP)
- Studied how email is sent between clients and servers
- Reviewed SMTP commands:
  - HELO / EHLO
  - MAIL FROM
  - RCPT TO
  - DATA
- Used `telnet` to manually send an email
- Default port: TCP 25

![image ult](https://github.com/CodedByCarlosC/Network-Core-Protocols/blob/5e4cb2df8454b94f90e203b0d906d6019a02dac8/SENDING%20EMAIL%20TELNET.PNG)

---

### 🔹 POP3 vs IMAP

**POP3**
- Designed to download emails to a single client
- Messages are typically deleted from the server
- Commands explored:
  - USER, PASS, STAT, LIST, RETR, DELE
- Default port: TCP 110

![image ult](https://github.com/CodedByCarlosC/Network-Core-Protocols/blob/5e4cb2df8454b94f90e203b0d906d6019a02dac8/POP3.PNG)

**IMAP**
- Designed for synchronized mailboxes across devices
- Emails remain on the server
- Supports folders and message state syncing
- Default port: TCP 143

---

## 🔐 Default Ports Summary

| Protocol | Transport | Default Port |
|--------|----------|--------------|
| TELNET | TCP | 23 |
| DNS | UDP / TCP | 53 |
| HTTP | TCP | 80 |
| HTTPS | TCP | 443 |
| FTP | TCP | 21 |
| SMTP | TCP | 25 |
| POP3 | TCP | 110 |
| IMAP | TCP | 143 |

---

## 🛡️ Security Takeaways

- Many protocols transmit sensitive data in plaintext
- Protocol knowledge is essential for traffic analysis
- Understanding commands helps identify abuse and misconfigurations
- Wireshark visibility is critical for investigation and troubleshooting
- Secure variants (e.g., HTTPS, SMTPS, IMAPS) mitigate risks

---

## 📌 Why This Matters for Cybersecurity

Understanding core protocols is foundational for:
- SOC analysis
- Network troubleshooting
- Packet analysis
- Incident response
- Threat detection and investigation

This lab strengthened my ability to reason about network traffic and identify normal vs suspicious behavior.

