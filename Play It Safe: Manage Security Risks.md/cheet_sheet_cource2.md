# 🛡️ Course 2 Master Cheat Sheet: Security Frameworks, Controls, and Operations

## 🎯 Overview
This master study guide compiles the foundational principles of organizational security, risk management frameworks, the 8 CISSP domains, and the operational tools (SIEM/SOAR/Playbooks) used by Security Operations Centers (SOCs) to maintain business continuity.

---

## 📐 Part 1: InfoSec Foundations & Risk

### The CIA Triad
The foundational model that informs how organizations consider risk and establish security policies.
| Principle | Definition | Implementation Example |
| :--- | :--- | :--- |
| **Confidentiality** | Ensuring only authorized users can access specific assets. | Principle of Least Privilege, Encryption. |
| **Integrity** | Ensuring data is verifiably correct, authentic, and reliable. | Cryptography, Hashing (preventing tampering). |
| **Availability** | Ensuring data/systems are accessible to authorized users. | Network redundancy, robust remote access, backups. |

### The Threat Landscape Lexicon
* **Asset:** An item perceived as having value to an organization (Digital = PII, Physical = Servers).
* **Vulnerability:** A weakness that can be exploited by a threat.
* **Threat:** Any circumstance or event that can negatively impact assets (Internal vs. External).
* **Attack Vectors:** The pathways attackers use to penetrate security defenses.
* **Risk:** Anything that can impact the confidentiality, integrity, or availability of an asset.
> **Risk Assessment Formula:** `Risk = Likelihood of a Threat × Impact to the Asset`

### Risk Management Strategies
1. **Mitigation:** Lessening the impact of a known risk (e.g., installing firewalls).
2. **Transference:** Transferring risk to a third party (e.g., buying cyber insurance).
3. **Avoidance:** Creating a plan to avoid the risk altogether.
4. **Acceptance:** Accepting a risk to avoid disrupting business continuity.

---

## 🏛️ Part 2: Security Frameworks & Controls

* **Security Frameworks:** High-level guidelines for risk mitigation and compliance (e.g., NIST, ISO 27001, OWASP).
* **Security Controls:** Specific safeguards (Physical, Technical/Logical, and Administrative) designed to reduce risk.
* **Security Audit:** A review of an organization's security controls and procedures against a set of expectations/laws.

### NIST Cybersecurity Framework (CSF)
A continuous, lifecycle approach to managing cybersecurity risk:
1. **Govern:** Establish organizational structures and leadership commitment.
2. **Identify:** Map out assets, people, and data to understand the attack surface.
3. **Protect:** Implement safeguards (policies, training, firewalls) to mitigate threats.
4. **Detect:** Utilize monitoring capabilities to identify active incidents quickly.
5. **Respond:** Execute procedures to contain and neutralize security incidents.
6. **Recover:** Restore affected systems back to normal operations.

### NIST Risk Management Framework (RMF)
A 7-step process to manage security and privacy risks. *(Memory Trick: P-C-S-I-A-A-M)*
1. **Prepare:** Activities necessary to manage risk *before* a breach occurs.
2. **Categorize:** Develop risk management processes based on system impact.
3. **Select:** Choose and document the controls that protect the organization.
4. **Implement:** Put the security and privacy plans into action.
5. **Assess:** Determine if established controls are implemented correctly.
6. **Authorize:** Senior leadership signs off and accepts accountability for risks.
7. **Monitor:** Be continuously aware of how systems are operating.

### OWASP Secure Software Principles
* **Establish Secure Defaults:** Highly secure out-of-the-box.
* **Fail Securely:** If a system fails, it must default to a secure, closed state.
* **Avoid Security by Obscurity:** Rely on strong architecture, not on keeping code a secret.
* **Defense in Depth:** Use multiple, layered security controls.

---

## 🌐 Part 3: The 8 Domains of Cybersecurity (CISSP)

1. **Security and Risk Management:** Focuses on security posture, compliance, ethics, and business continuity.
2. **Asset Security:** Managing the lifecycle of physical and virtual data (storage, retention, destruction).
3. **Security Architecture and Engineering:** Designing secure systems using Threat Modeling and Zero Trust.
4. **Communication and Network Security:** Securing physical and wireless networks (especially for remote workers).
5. **Identity and Access Management (IAM):** Authenticating users and enforcing the Principle of Least Privilege.
6. **Security Assessment and Testing:** Auditing controls and performing Penetration Testing.
7. **Security Operations:** Active investigations, log management, SIEM utilization, and incident response.
8. **Software Development Security:** Baking security into the Software Development Life Cycle (SDLC) from day one.

---

## ⚙️ Part 4: Security Operations (SOC Tools & Incident Response)

### SIEM vs. SOAR
* **SIEM (Security Information and Event Management):** Collects and analyzes log data to monitor critical activities and alert teams of potential threats (e.g., *Splunk, Google Chronicle*). Requires human analysis.
* **SOAR (Security Orchestration, Automation, and Response):** Workflows that use automation to instantly respond to security events without waiting for a human.

### The Incident Response Playbook
A **Playbook** is an operational manual providing a predefined list of steps to perform when responding to a specific incident (e.g., Ransomware). It is a "living document" updated after failures or landscape changes.

**The 6 Steps of Incident Response:**
1. **Preparation:** Establishing readiness before an attack.
2. **Detection:** Identifying the threat.
3. **Analysis:** Investigating scope and origin.
4. **Containment:** Isolating systems to stop the spread.
5. **Eradication:** Removing the vulnerability/attacker.
6. **Recovery:** Restoring normal operations.

---

## 📖 Part 5: Core Glossary & Terminology

* **Authentication:** The process of verifying *who* someone is (e.g., passwords, biometrics).
* **Authorization:** The process of granting access to specific resources *after* authentication.
* **Biometrics:** Unique physical characteristics used to verify identity (e.g., fingerprints).
* **Encryption:** Converting data from a readable format to an encoded format.
* **Incident Response:** An organization’s quick attempt to identify an attack, contain damage, and correct effects.
* **Log:** A record of events that occur within an organization’s systems.
* **Metrics:** Key technical attributes (response time, availability) used to assess software performance.
* **Operating System (OS):** The interface between computer hardware and the user (e.g., Linux).
* **Ransomware:** A malicious attack where actors encrypt data and demand payment for its return.

---

# 🚦 Course 2 Exam Prep: The Triage Guide

## 🚨 Tier 1: MUST REMEMBER (The Non-Negotiables)
*If you wake up at 3:00 AM and someone asks you these, you need to know them instantly. These are the core foundations of the entire cybersecurity industry.*

* **The CIA Triad:**
  * **Confidentiality:** Only authorized people get access (Encryption).
  * **Integrity:** The data hasn't been altered or tampered with (Hashing).
  * **Availability:** The system is actually up and running when needed (Backups).
* **The Core 4 Security Terms:**
  * **Asset:** What you are protecting (Data, Servers).
  * **Threat:** Who/What is attacking (Hackers, Natural Disasters).
  * **Vulnerability:** The weakness they use to get in (Unpatched software).
  * **Risk:** The intersection of all three. **(Risk = Threat × Vulnerability/Impact)**.
* **SIEM vs. SOAR:**
  * **SIEM (The Brain):** Collects logs and flags threats. *Requires human analysis.*
  * **SOAR (The Muscle):** Uses automation to instantly respond to threats *without* a human.
* **The 6 Steps of Incident Response (The Playbook):**
  1. Preparation 
  2. Detection 
  3. Analysis 
  4. Containment 
  5. Eradication 
  6. Recovery
* **The NIST Cybersecurity Framework (CSF) Core Functions:**
  Govern ➔ Identify ➔ Protect ➔ Detect ➔ Respond ➔ Recover.

---

## ⚠️ Tier 2: SLIGHTLY LESS BUT IMPORTANT (Frameworks & Application)
*You will likely see multiple-choice questions on these. You need to know the definitions and be able to spot the differences between them.*

* **Risk Treatment Strategies:**
  * **Mitigate:** Lessen the impact (Buy a firewall).
  * **Transfer:** Make it someone else's problem (Buy cyber insurance).
  * **Avoid:** Don't do the risky thing at all.
  * **Accept:** Accept the risk because the business needs to keep running.
* **Security Controls (The 3 Types):**
  * **Physical:** Fences, security guards, biometric locks.
  * **Technical (Logical):** Firewalls, antivirus, encryption.
  * **Administrative:** Employee training, security policies, separation of duties.
* **The NIST Risk Management Framework (RMF):**
  * Just remember the acronym flow: **P-C-S-I-A-A-M** (Prepare, Categorize, Select, Implement, Assess, Authorize, Monitor).
* **The 8 CISSP Domains (General Themes):**
  * Focus heavily on **Domain 5 (IAM - Identity & Access Management)** and the *Principle of Least Privilege*.
  * Focus heavily on **Domain 7 (Security Operations)** because that is where incident response, SIEM, and SOC analysts live.

---

## 🧠 Tier 3: JUST REMEMBER IT FOR KNOWLEDGE (Context)
*You don't need to memorize these word-for-word. Just understand the general concepts so you have context when senior engineers talk about them.*

* **Specific SIEM Dashboard Names:**
  * You don't need to memorize every single tab in Splunk or Chronicle. Just know that dashboards exist to track *Security Posture*, *IOC Matches* (Indicators of Compromise), and *User Sign-ins*.
* **Open-Source vs. Proprietary:**
  * Open-Source (Linux, Suricata) = Free, code is public, patched quickly by the community.
  * Proprietary (Splunk) = Paid, code is hidden, patched officially by the company.
* **OWASP Secure Software Principles:**
  * Know the concepts of **Fail Securely** (if a system breaks, it should lock down, not open up) and **Defense in Depth** (having multiple layers of security).
* **Basic IT Definitions:**
  * Don't stress over memorizing the textbook definitions for things like *Metrics*, *Log*, or *Operating System*. As long as you know what they are practically, you are fine.
* **Security Posture:** An organization’s ability to manage its defense of critical assets and react to change.
* **Shared Responsibility:** The idea that all individuals in an organization take an active role in lowering risk.
* **Social Engineering:** A manipulation technique that exploits human error to gain private information.
