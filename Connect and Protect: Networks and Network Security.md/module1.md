# 🌐 Network Architecture & Fundamentals (Course 3, Module 1)

This repository contains my core technical notes, architectural breakdowns, and foundational concepts from Module 1 of the Google Cybersecurity Certificate (**Course 3: Connect and Protect**). It covers physical network hardware, layered communication models, and the shift from on-premise infrastructure to cloud environments.

---

## 🏗️ Network Topologies & Core Hardware

A network is a group of connected devices that share information. Networks generally fall into two physical scopes:
* **LAN (Local Area Network):** Spans a small area like a home, school, or single office building.
* **WAN (Wide Area Network):** Spans large geographic areas like cities or countries (e.g., the Internet).

### The Hardware Stack
| Device | Description | Security / Performance Impact |
| :--- | :--- | :--- |
| **Hub** | Connects devices but broadcasts information to *every* port. | **Vulnerable:** Highly susceptible to packet sniffing; rarely used in modern setups. |
| **Switch** | Connects local devices and forwards traffic *only* to the intended destination. | **Secure:** Uses a MAC address table to direct traffic, improving speed and security. |
| **Router** | Connects multiple distinct networks together (e.g., a LAN to the Internet). | **Vital:** Directs traffic based on IP addresses; often features built-in firewalls. |
| **Modem** | Connects the local router to the Internet Service Provider (ISP). | Converts digital signals for transmission over physical lines (fiber, coaxial). |
| **Firewall** | Security device monitoring incoming/outgoing traffic. | Acts as the first line of defense between internal networks and the untrusted internet. |
| **WAP** | Wireless Access Point. | Broadcasts digital signals over radio waves utilizing Wi-Fi standards. |

---

## ☁️ Enterprise Infrastructure: The Cloud

Modern organizations are shifting from traditional **On-Premise** networks (where all physical servers are owned and housed locally) to **Cloud Computing**—leveraging remote data centers accessed via the internet.

### Cloud Service Models
* **IaaS (Infrastructure as a Service):** Virtual computers, containers, and storage managed via an API.
* **PaaS (Platform as a Service):** Frameworks and tools for developers to build custom applications.
* **SaaS (Software as a Service):** Fully functional, web-hosted software suites.

### Deployment & Virtualization
* **Hybrid Cloud:** Combining on-premise hardware with Cloud Service Provider (CSP) resources.
* **Multi-Cloud:** Utilizing multiple CSPs simultaneously to distribute risk.
* **SDN (Software-Defined Networks):** Virtualized routers, switches, and firewalls that perform packet routing via software rather than physical hardware. 

> **Why Cloud?** It offers high **Reliability** (consistent uptime), decreased **Cost** (no massive upfront hardware purchases), and extreme **Scalability** (elastic resources that grow or shrink with demand).

---

## 🗺️ Network Communication Models

To understand how a data packet travels from a physical cable up to a web browser, engineers rely on standardized layered frameworks.

### The OSI Model (7 Layers)
1. **Physical:** Raw 0s and 1s transmitted over cables/radio waves.
2. **Data Link:** Organizes packets within a local network using switches and MAC addresses.
3. **Network:** Routes data between different networks using routers and IP addresses.
4. **Transport:** Handles delivery speed, flow control, and segmentation (TCP/UDP).
5. **Session:** Establishes, maintains, and terminates connections (checkpoints).
6. **Presentation:** Handles data formatting, translation, and encryption (e.g., SSL).
7. **Application:** End-user software protocols (HTTP, DNS, SMTP).

### The TCP/IP Model (4 Layers)
A streamlined framework heavily used in modern networking:
1. **Network Access Layer:** Corresponds to OSI Layers 1 & 2 (MAC addresses, ARP).
2. **Internet Layer:** Corresponds to OSI Layer 3 (IP addressing, ICMP routing).
3. **Transport Layer:** Corresponds to OSI Layer 4 (TCP / UDP delivery).
4. **Application Layer:** Corresponds to OSI Layers 5, 6, & 7 (HTTP, SSH, FTP).

---

## 📦 Data Packets & Protocols

A **Data Packet** is the basic unit of information traveling across a network. It relies on specific protocols to reach its destination.

### Addressing
* **IP Address:** A unique logical string routing a device on the internet.
* **MAC Address:** A physical, hardcoded alphanumeric identifier for a device's network card.
* **Port:** A software-based location organizing traffic for specific services (e.g., Port 443 for Secure Internet, Port 25 for Email).

### Transport Protocols
* **TCP (Transmission Control Protocol):** Connection-oriented. Ensures reliable, tracked delivery (e.g., file downloads).
* **UDP (User Datagram Protocol):** Connectionless. Fast, untracked delivery (e.g., live video streaming).

### The IPv4 Packet Header Anatomy
An IPv4 header ranges from 20 to 60 bytes and contains 13 critical routing fields:
1. **Version (VER):** Protocol identifier (IPv4).
2. **IP Header Length (IHL):** Where the header ends and data begins.
3. **Type of Service (ToS):** Traffic prioritization.
4. **Total Length:** Max size is 65,535 bytes.
5. **Identification:** Fragment tracker.
6. **Flags:** Fragmentation status.
7. **Fragmentation Offset:** Reassembly order.
8. **Time to Live (TTL):** Hop counter to prevent infinite looping.
9. **Protocol:** Inner payload identifier (TCP/UDP).
10. **Header Checksum:** Corruption detection.
11. **Source IP Address:** Sender location.
12. **Destination IP Address:** Target location.
13. **Options:** Custom security configurations.

> **The IPv6 Shift:** Due to IPv4 address exhaustion (4.3 billion limit), the world is migrating to **IPv6**—utilizing 16-byte hexadecimal addresses that provide 340 undecillion unique combinations and a simplified, faster packet header.

---
*Documented by a BSc CS student building a foundation for Cloud Security Engineering.*
