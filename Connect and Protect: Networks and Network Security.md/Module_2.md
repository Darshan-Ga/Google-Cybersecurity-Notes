# Course 3, Module 2: Network Security Architecture
**Google Cybersecurity Certificate**

This module shifts the focus from how networks are built to how they are defended. It covers the core security architecture, including communication protocols, wireless security standards, subnetting, firewalls, and virtual private networks (VPNs).

---

## 1. Network Protocols & Ports
Protocols are the established rules that determine how data is transmitted between different devices in the same network. 

| Protocol | Port | Category | Description |
| :--- | :--- | :--- | :--- |
| **TCP** | N/A | Communication | Transmission Control Protocol. Establishes a reliable, tracked connection using a three-way handshake. |
| **UDP** | N/A | Communication | User Datagram Protocol. Connectionless and fast, but does not guarantee delivery. |
| **HTTP** | 80 | Communication | Hypertext Transfer Protocol. Unsecured web communication. |
| **HTTPS** | 443 | Security | Secure version of HTTP using SSL/TLS encryption. |
| **DNS** | 53 | Communication | Domain Name System. Translates domain names into IP addresses (usually UDP). |
| **DHCP** | 67/68 | Management | Dynamic Host Configuration Protocol. Automatically assigns IP addresses to devices. |
| **ARP** | N/A | Management | Address Resolution Protocol. Maps an IP address to a physical MAC address on a local network. |
| **ICMP** | N/A | Management | Internet Control Message Protocol. Reports errors and network connectivity (e.g., `ping`). |
| **SNMP** | 161/162 | Management | Simple Network Management Protocol. Monitors and manages network devices. |
| **SSH** | 22 | Security | Secure Shell. Creates a secure, encrypted terminal session with a remote system. |
| **Telnet** | 23 | Communication | Legacy remote access protocol. Sends data in clear text (Insecure; replaced by SSH). |
| **SFTP** | 22 | Security | Secure File Transfer Protocol. Uses SSH to securely transfer files. |
| **SMTP** | 25/587 | Communication | Simple Mail Transfer Protocol. Routes and sends outgoing emails. |
| **POP3** | 110/995 | Communication | Post Office Protocol. Downloads emails to a local device (usually deletes from server). |
| **IMAP** | 143/993 | Communication | Internet Message Access Protocol. Syncs incoming emails across multiple devices. |

---

## 2. Network Organization & Addressing
Proper network segmentation improves both speed and security by containing traffic and isolating potential breaches.

* **Subnetting:** The process of dividing one large network into smaller, organized groups (subnets) to create security zones.
* **CIDR (Classless Inter-Domain Routing):** A modern method of assigning subnet masks to IP addresses (e.g., `198.51.100.0/24`), expanding the available number of IPv4 addresses.
* **NAT (Network Address Translation):** A router/firewall process that translates private IP addresses on a local network into a single public IP address for internet communication.

---

## 3. Wireless Security Standards (IEEE 802.11)
Wireless networks use radio waves to transmit data, making encryption critical to prevent packet sniffing.

* **WEP (Wired Equivalent Privacy):** The oldest standard (1999). Highly vulnerable and easily broken.
* **WPA (Wi-Fi Protected Access):** Introduced TKIP to improve encryption but remains vulnerable to attacks.
* **WPA2:** The current standard. Uses strong AES encryption and CCMP. Vulnerable to KRACK (Key Reinstallation Attacks). Available in Personal (shared password) and Enterprise (individual user keys) modes.
* **WPA3:** The modern, highly secure standard. Uses Simultaneous Authentication of Equals (SAE) to prevent dictionary attacks and features 128-bit/192-bit encryption.

---

## 4. Defending the Network: Firewalls & Proxies
These devices sit at the boundary of a network to monitor and filter incoming and outgoing traffic.

* **Stateless Firewall:** Filters traffic based on predefined rules (IP address and port) without remembering past connections.
* **Stateful Firewall:** Tracks the "state" of active connections and proactively filters threats. Only requires rules in one direction.
* **Next-Generation Firewall (NGFW):** Performs deep packet inspection at the application layer, integrating intrusion prevention, malware sandboxing, and DNS filtering.
* **Forward Proxy Server:** Protects internal clients by regulating and intercepting their requests to the public internet.
* **Reverse Proxy Server:** Protects internal servers by intercepting and regulating requests coming from the public internet.

---

## 5. Virtual Private Networks (VPNs)
VPNs use **encapsulation** to wrap unencrypted data inside an encrypted data packet, creating a secure tunnel over a public network.

* **Remote Access VPN:** Connects an individual user's device securely to a remote network.
* **Site-to-Site VPN:** Connects two entirely separate networks together (e.g., two different office branches) securely over the internet.
* **IPSec:** A highly secure, extensively tested, and traditional VPN protocol.
* **WireGuard:** A modern, open-source VPN protocol known for high speeds, advanced encryption, and a lightweight codebase.

---

## Glossary of Key Terms
* **Bandwidth:** The maximum data transmission capacity over a network.
* **Controlled Zone:** A subnet that protects the internal network from the uncontrolled zone.
* **Encapsulation:** Wrapping sensitive data within other data packets for secure transit.
* **Packet Sniffing:** Capturing and inspecting data packets across a network.
* **Port Filtering:** Blocking or allowing certain port numbers to limit communication.
* **Security Zone:** A segment of a network protecting internal resources from the internet.
* **Uncontrolled Zone:** The portion of the network outside the organization (the public internet).

---
*First-year CS student. Target: Cloud Security Engineering. Building in public. 🔐*
[github.com/Darshan-Ga](https://github.com/Darshan-Ga)
