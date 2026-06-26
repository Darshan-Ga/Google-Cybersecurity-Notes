# 🛡️ Connect and Protect: Networks and Network Security - Module 4

## 📖 Overview
This repository contains notes and concepts from **Module 4 of the Google Cybersecurity Certificate**. The module focuses on strengthening network defenses, analyzing network traffic for malicious activity, implementing layered security architectures, and applying security frameworks to cloud computing environments.

---

## 🏗️ 1. Network Security Devices & Architecture
To achieve maximum security, networks utilize a layered approach to monitor, filter, and stop malicious traffic.

* **Defense in Depth:** The overarching strategy of using multiple, overlapping layers of security (e.g., Firewalls + IPS + MFA + Encryption). If an attacker bypasses one layer, the next layer stops them.
* **Network Segmentation:** Dividing a large network into smaller sub-networks (like VLANs). If malware infects one department, segmentation prevents it from easily spreading to others.
* **Firewall:** The first line of defense. It allows or blocks traffic based on a strict set of rules by inspecting packet headers (port numbers and IP addresses). 
    * **Stateless Firewalls:** Only look at the static rules and packet headers. Fast, but easily tricked.
    * **Stateful Firewalls:** Remember the "state" of the connection. They track the entire conversation from start to finish, making them much more secure against spoofing attacks.
* **Intrusion Detection System (IDS):** Sits behind the firewall. It passively monitors network traffic for signatures of known attacks or suspicious anomalies. It **alerts** administrators but *does not* actively stop the traffic.
* **Intrusion Prevention System (IPS):** Sits inline behind the firewall. It actively monitors traffic and **takes action** to drop packets or block senders if malicious activity is detected. *Risk: Can accidentally block legitimate traffic (false positives) or break the network connection if the appliance fails.*
* **Security Information and Event Management (SIEM):** Tools (like Splunk or Google Chronicle) that aggregate and analyze log data from Firewalls, IDS, IPS, and servers into a single centralized dashboard for security analysts to monitor.
* **Full Packet Capture Devices:** Tools used to record and analyze all data transmitted over the network, heavily used during incident response and alert investigation.

---

## 🔒 2. System Vulnerabilities & Prevention

### Brute Force Attacks
A trial-and-error method used by attackers to guess login credentials.
* **Simple Brute Force:** Guessing random combinations of usernames and passwords.
* **Dictionary Attack:** Using automated lists of commonly used passwords or credentials stolen in previous data breaches.

### Prevention Measures
* **Salting and Hashing:** Hashing converts passwords into one-way cryptographic text. Salting adds random characters to the hash, making it exponentially harder to crack.
* **Multi-Factor Authentication (MFA / 2FA):** Requires users to verify identity using two or more methods (e.g., password + SMS code, badge, or biometric scan).
* **CAPTCHA:** Automated tests to prove a user is human, stopping bots from rapidly guessing passwords.
* **Password Policies:** Enforcing rules like password length, expiration dates, and account lockouts after failed attempts.

### Safe Testing Environments
* **Virtual Machines (VMs):** Software versions of physical computers. Used to run potentially malicious code in an isolated environment without harming the host network.
* **Sandbox Environments:** Isolated testing environments used to evaluate suspicious files, test patches, or simulate attack scenarios safely. *Note: Advanced malware can sometimes detect when it is inside a VM or sandbox and hide its malicious behavior.*

---

## 🛠️ 3. Security Hardening Tasks
Security hardening is the process of strengthening a system to reduce its vulnerability and attack surface.

| Task | Description | Common Use |
| :--- | :--- | :--- |
| **Baseline Configurations** | Documented specifications for how a secure system should be built. | Used to restore systems to a known secure state after an outage or breach. |
| **Port Filtering** | Blocking or allowing specific port numbers on firewalls and routers. | Prevents attackers from exploiting unused open ports. |
| **Network Access Privileges** | Limiting access based on roles, IPs, or MAC addresses. | Reduces the risk of insider threats and unauthorized access. |
| **Encryption Updates** | Utilizing the latest standards to conceal data. | Protecting data in transit and at rest from interception. |
| **Firewall Maintenance** | Checking and updating security configurations regularly. | Updating rules in response to abnormal traffic or DDoS attacks. |
| **Patch Updates** | Software/OS updates that address vulnerabilities. | Closing security gaps before attackers can exploit them. |
| **Network Log Analysis** | Examining network logs to identify events of interest. | Configuring SIEM alerts for abnormal traffic before or during an attack. |
| **Hardware/Software Disposal** | Properly wiping data from old assets. | Preventing data recovery from discarded or unpatched legacy devices. |
| **Penetration Testing** | Simulated attacks to identify vulnerabilities. | Proactively finding network flaws before malicious actors do. |
| **Data Storage Backups** | Recording and storing copies of critical data. | Restoring data lost to ransomware, hardware failure, or human error. |

---

## ☁️ 4. Cloud Security Fundamentals
Cloud computing (ease of deployment, scalability, cost savings) introduces unique security challenges, primarily an expanded attack surface and complex configurations. 

### The Shared Responsibility Model
The fundamental rule of cloud security:
* **Cloud Service Provider (CSP):** Responsible for the security **OF** the cloud (physical data centers, host OS, hardware, and hypervisors).
* **Customer/Organization:** Responsible for security **IN** the cloud (data, applications, IAM configurations, and user access).

### Cloud Hardening Techniques
* **Identity Access Management (IAM):** Strict control over user roles and digital identities to prevent unauthorized access to critical cloud operations.
* **Hypervisor Security:** Protecting the software that creates Virtual Machines. CSPs use Type 1 (bare metal) hypervisors and secure them to prevent "VM Escapes" (where an attacker breaks out of a VM to access the host computer).
* **Baselining:** Establishing a fixed reference point for cloud setup (e.g., restricting admin portal access, enabling file encryption).

### Cryptography & Key Management in the Cloud
* **Cryptography:** Encrypting data stored in the cloud. Modern encryption relies on the secrecy of the *key*, not the algorithm.
* **Hardware Security:** Encryption keys are stored securely using:
    * **TPM (Trusted Platform Module):** A secure computer chip that stores certificates and keys.
    * **CloudHSM:** A computing device that securely processes cryptographic operations.
* **Cryptographic Erasure (Crypto-shredding):** Permanently destroying the encryption keys, rendering the associated cloud data completely undecipherable and permanently inaccessible.

---

## 🕵️ 5. Network Traffic Analysis (tcpdump Example)
Analyzing network logs is crucial for detecting compromises, such as DNS spoofing or malicious downloads.

**1. The Initial DNS Request**
```text
14:18:32.192571 IP your.machine.52444 > dns.google.domain: 35084+ A? yummyrecipesforme.com. (24)
14:18:32.204388 IP dns.google.domain > your.machine.52444: 35084 1/0/0 A 203.0.113.22 (40)
```
The host machine asks the DNS server for the IP of yummyrecipesforme.com and receives 203.0.113.22.

**2. The TCP Handshake & HTTP GET Request**
```text
14:18:36.786501 IP your.machine.36086 > yummyrecipesforme.com.http: Flags [S]...
14:18:36.786517 IP yummyrecipesforme.com.http > your.machine.36086: Flags [S.]...
14:18:36.786589 IP your.machine.36086 > yummyrecipesforme.com.http: Flags [P.], ... HTTP: GET / HTTP/1.1
```

The host establishes a connection ([S] Connection Start, [S.] Acknowledgment) and pushes a request to download data ([P.] Data Push with HTTP: GET).

**3. The Redirection (Malicious Activity)**
```text
14:20:32.192571 IP your.machine.52444 > dns.google.domain: 21899+ A? greatrecipesforme.com. (24)
14:20:32.204388 IP dns.google.domain > your.machine.52444: 21899 1/0/0 A 192.0.2.172 (40)
14:25:29.576493 IP your.machine.56378 > greatrecipesforme.com.http: Flags [S]...
```
The traffic is suddenly routed to a new, spoofed domain (greatrecipesforme.com) at a different IP address (192.0.2.172), indicating a potential network compromise or malicious redirect.




