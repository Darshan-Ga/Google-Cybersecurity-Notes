# 🛡️ Foundation of Cybersecurity: Risk Management & The 8 Domains

## 🎯 Overview
This repository contains comprehensive notes and practical insights on organizational security posture, the NIST Risk Management Framework (RMF), and the 8 core CISSP domains of cybersecurity. The primary objective is to understand how to protect digital and physical assets from internal and external threats while maintaining business continuity.

---

## 📐 Core Principles of Information Security (InfoSec)
**Information Security (InfoSec)** refers to the set of processes established to secure information. Every security control ultimately ties back to the **CIA Triad**:
* **Confidentiality:** Only authorized people can view the data (e.g., Encryption).
* **Integrity:** Data is accurate, unaltered, and trustworthy (e.g., File hashing).
* **Availability:** Data and systems are accessible when needed (e.g., Server backups).

---

## 📖 The Security Lexicon: Threats, Risks & Vulnerabilities

### 1. Assets
An **Asset** is anything perceived as having value to an organization.
* **Digital Assets:** Social Security Numbers (SSNs), dates of birth, bank account numbers, mailing addresses (PII).
* **Physical Assets:** Payment kiosks, servers, desktop computers, office spaces.

### 2. Vulnerabilities
A **Vulnerability** is a weakness in a system that can be exploited by a threat.

### 3. Threats
A **Threat** is any circumstance or event that can negatively impact assets.
* **Internal Threat:** A current/former employee, vendor, or trusted partner who poses a security risk.
* **Insider Threat:** Staff or vendors abusing their *authorized* access to obtain data.
* **External Threat:** Anything outside the organization attempting to harm assets.
* **Advanced Persistent Threat (APT):** A threat actor maintaining unauthorized access to a system for an extended period of time.
* **Ransomware:** A malicious attack where threat actors encrypt data and demand payment to restore access.
* **Social Engineering:** A manipulation technique exploiting human error to gain private information or access.

### 4. Risk
**Risk** is anything that can impact the confidentiality, integrity, or availability of an asset.
* **Formula:** `Risk = Likelihood of a Threat × Impact to the Asset`

#### ⚠️ Factors that affect the likelihood of a Risk:
1. **External Risk:** Outside threat actors attempting to gain access.
2. **Internal Risk:** Trusted personnel causing harm (intentionally or accidentally).
3. **Legacy Systems:** Old systems (e.g., old mainframe systems or vending machines) that are unaccounted for or cannot be updated.
4. **Multiparty Risk:** Outsourcing work to third-party vendors, giving them access to intellectual property (trade secrets, software designs).
5. **Software Compliance/Licensing:** Software that is not updated, not in compliance, or lacking timely patches.

---

## 🚦 Risk Management & Frameworks
Organizations implement risk management processes based on widely accepted frameworks like the **NIST RMF**, **HITRUST** (Health Information Trust Alliance), and the **OWASP Top 10** (for web application security).

### Risk Management Strategies
| Strategy | Definition |
| :--- | :--- |
| **Mitigation** | Lessening the impact of a known risk (e.g., installing firewalls). |
| **Transference** | Transferring risk to a third party to manage (e.g., cyber insurance). |
| **Avoidance** | Creating a plan to avoid the risk altogether. |
| **Acceptance** | Accepting a risk to avoid disrupting business continuity. |

---

## 🏗️ The NIST Risk Management Framework (RMF)
The NIST RMF is a 7-step process to manage security and privacy risks effectively. 
*(Memory Trick: P-C-S-I-A-A-M)*

1. **Prepare:** Activities necessary to manage security and privacy risks *before* a breach occurs.
2. **Categorize:** Used to develop risk management processes and tasks based on system impact.
3. **Select:** Choose, customize, and capture documentation of the controls that protect the organization.
4. **Implement:** Implement the chosen security and privacy plans.
5. **Assess:** Determine if established controls are implemented correctly and functioning as intended.
6. **Authorize:** Senior leadership acts accountable for the security/privacy risks and signs off on the system.
7. **Monitor:** Be continuously aware of how systems are operating and watch for new changes.

---

## 🌐 The 8 Domains of Cybersecurity

### Domain 1: Security and Risk Management
Focuses on the organization's **Security Posture** (ability to manage defense and react to change) and **Business Continuity** (maintaining everyday productivity via disaster recovery plans). 
* **Key Elements:** Security goals, risk mitigation, compliance (e.g., GDPR), legal regulations, and ethics.
* **InfoSec Design Processes:** Incident response, vulnerability management, application security, cloud security, infrastructure security.

### Domain 2: Asset Security
Focuses on managing the lifecycle of physical and virtual data. 
* **Key Elements:** Storage, maintenance, retention, and secure destruction of data.
* **Tasks:** Conducting security impact analysis, establishing recovery plans, managing data exposure, and creating backups.

### Domain 3: Security Architecture and Engineering
Focuses on managing data security by ensuring effective tools and systems are in place.
* **Shared Responsibility:** All individuals take an active role in lowering risk during system design.
* **Core Design Principles:**
  1. Threat modeling
  2. Least privilege
  3. Defense in depth
  4. Fail securely
  5. Separation of duties
  6. Keep it simple
  7. Zero trust
  8. Trust but verify
* **Tools:** Utilizing SIEM (Security Information and Event Management) to monitor unusual logins.

### Domain 4: Communication and Network Security
Focuses on managing and securing physical networks and wireless communications (on-site, remote, and cloud).
* **Key Challenge:** Designing network security controls (restricted access) to protect hybrid/remote workers accessing networks from outside the main office.

### Domain 5: Identity and Access Management (IAM)
Focuses on keeping data secure by ensuring user identities are trusted/authenticated and access is authorized.
* **Core Concept:** The **Principle of Least Privilege** (granting only the minimal access required to complete a task, and removing it when the task is done).

### Domain 6: Security Assessment and Testing
Focuses on identifying and mitigating risks, threats, and vulnerabilities.
* **Key Elements:** Conducting security control testing, collecting/analyzing data, and performing security audits to reduce breach probability.
* **Roles:** Employing Penetration Testers ("pen testers") to find exploitable vulnerabilities, and auditing user permissions.

### Domain 7: Security Operations
Focuses on the investigation of potential breaches and preventative measures after an incident.
* **Strategies, Processes & Tools Include:**
  * Training and awareness
  * Reporting and documentation
  * Intrusion detection and prevention
  * SIEM tools
  * Log management
  * Incident management
  * Playbooks
  * Post-breach forensics
  * Reflecting on lessons learned (handling active attacks out of normal hours).

### Domain 8: Software Development Security
Focuses on using secure programming practices to create reliable applications.
* **Core Concept:** Security must be incorporated into every element of the Software Development Life Cycle (SDLC) from design to release. It cannot be an afterthought.
* **Key Tasks:** Performing application security tests, testing programming conventions/executables, and ensuring QA meets performance standards (e.g., configuring proper encryption for software).
