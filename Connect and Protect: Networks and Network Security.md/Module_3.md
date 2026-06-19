# 🛡️ Network Attacks & Packet Analysis

This repository contains notes and practical incident response summaries regarding network vulnerabilities, interception techniques, Denial of Service (DoS) attacks, and packet analysis using industry-standard tools like `tcpdump` and Wireshark. 

---

## 🎯 Threat Landscape & Attacker Motivations
Every network has inherent vulnerabilities. Malicious actors target networks for various reasons, including financial gain, personal/political motives, or insider threats (e.g., disgruntled employees). 

**Impacts of a Network Attack:**
* **Financial:** Loss of revenue due to downtime, ransom payments, or litigation costs from compromised client data.
* **Reputation:** Loss of public trust and customers turning to competitors.
* **Public Safety:** Compromise of government networks, power grids, or water systems.

---

## 🕵️‍♂️ Network Interception & Spoofing
Interception attacks work by capturing or interfering with data in transit across a network.

* **Packet Sniffing:** Using hardware or software to capture and inspect data packets in transit.
    * **Passive Packet Sniffing:** Connecting to a network hub to silently monitor and copy all network traffic without interaction.
* **On-Path Attack (Man-in-the-Middle):** A malicious actor places themselves between two trusted devices, intercepting, reading, or altering the data in transit. *(Mitigation: Strong encryption like TLS).*
* **Replay Attack:** Intercepting a legitimate data packet and delaying or repeating it later to gain unauthorized access.
* **IP Spoofing:** Changing the source IP of a data packet to impersonate an authorized system, often used to bypass firewalls or hide the attacker's true identity.

---

## 💥 Denial of Service (DoS) Attacks
Unlike interception attacks that steal data, DoS attacks aim to overwhelm a system, preventing it from processing legitimate traffic.

* **DoS (Denial of Service):** Targets a network or server, flooding it with traffic from a *single* source.
* **DDoS (Distributed Denial of Service):** Uses a "botnet" (multiple infected devices across different locations) to flood the target, making it harder to stop.
* **SYN Flood Attack:** Exploits the TCP 3-way handshake. The attacker simulates a connection by sending massive amounts of `[SYN]` packets but never completes the handshake, exhausting the server's resources.
* **ICMP Flood Attack:** Overwhelming a network by repeatedly sending Internet Control Message Protocol (ICMP) echo requests (pings).
* **Ping of Death:** Sending an oversized, malformed ICMP packet (larger than 64KB) that causes the target system's memory to overflow and crash upon reassembly.
* **Smurf Attack:** Combining IP spoofing and ICMP. The attacker spoofs the victim's IP and sends a ping to a network's broadcast address, causing every device on that network to flood the victim with replies.

---

## 🚪 Backdoor Attacks
Backdoors are weaknesses intentionally left by programmers/admins to bypass normal access controls for troubleshooting. However, if attackers discover or install their own backdoors after compromising a system, they gain persistent, undetected access to install malware or steal data.

---

## 🔬 Network Protocol Analyzers
Protocol analyzers (packet sniffers) capture and format network traffic into readable logs. They are used to establish traffic baselines, troubleshoot performance, and detect malicious activity.
* **Common Tools:** `tcpdump`, Wireshark, SolarWinds NetFlow, Azure Network Watcher.

### `tcpdump`
A lightweight, command-line-based network protocol analyzer. 
* **Key Log Outputs:** Timestamp, Source IP & Port, Destination IP & Port, Protocol (TCP/UDP/ICMP), and Flags.

### Wireshark
A powerful graphical tool for analyzing network protocols.
* **Key Log Outputs:** Log entry number, Time (in milliseconds), Source/Destination IPs, Protocol (e.g., TCP, HTTP), and Info (e.g., ports, `[SYN]`, `[ACK]`, `[RST]`).

---

## 📝 Incident Response Scenarios

### Scenario 1: DNS Resolution Failure (`tcpdump` Analysis)
* **Symptom:** Users received "destination port unreachable" when trying to access a website.
* **Analysis:** A `tcpdump` capture showed outgoing UDP packets to a DNS server (port 53). The response was an ICMP error message: `udp port 53 unreachable`.
* **Conclusion:** The DNS server was not listening on port 53, preventing domain name resolution to an IP address.

### Scenario 2: Web Server Outage (Wireshark SYN Flood Analysis)
* **Symptom:** An automated monitoring system alerted of a web server problem. The website returned a "connection timeout" error.
* **Analysis:** Wireshark logs showed normal TCP 3-way handshakes (`[SYN]`, `[SYN, ACK]`, `[ACK]`) abruptly drowned out by rapid `[SYN]` requests from a single unfamiliar IP address. Legitimate users started receiving `504 Gateway Time-out` and `[RST, ACK]` (connection reset) errors.
* **Conclusion:** The web server was the victim of a direct SYN Flood DoS attack. The immediate mitigation involved taking the server offline to recover and configuring the firewall to block the attacking IP address.

---

## 📖 Glossary
* **ICMP:** Internet Control Message Protocol; used to communicate data transmission errors or check connectivity (ping).
* **TCP:** Transmission Control Protocol; a connection-oriented protocol requiring a handshake.
* **UDP:** User Datagram Protocol; a connectionless, "fire-and-forget" protocol.
