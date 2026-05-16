# 🛡️ Module 2: Security Frameworks, Controls, and Audits

## 🎯 Overview
This repository covers the foundational structures organizations use to defend data, maintain privacy, and adhere to legal compliance. It outlines the relationship between overarching security frameworks and the specific technical, physical, and administrative controls used to enforce them.

---

## 📐 The CIA Triad
The CIA triad is the foundational model that informs how organizations consider risk and establish their security posture.

| Principle | Definition | Implementation Example |
| :--- | :--- | :--- |
| **Confidentiality** | Ensuring only authorized users can access specific assets. | Principle of Least Privilege, Encryption. |
| **Integrity** | Ensuring data is verifiably correct, authentic, and reliable. | Cryptography, Hashing (preventing tampering). |
| **Availability** | Ensuring data/systems are accessible to authorized users. | Network redundancy, robust remote access, backups. |

---

## 🏛️ Frameworks vs. Controls
* **Security Frameworks:** The high-level guidelines used to build risk mitigation plans and achieve legal compliance (e.g., HIPAA). 
    * *CTF (Cyber Threat Framework):* A common language for describing cyber threat activity.
    * *ISO/IEC 27001:* An international standard for managing the security of assets and building an Information Security Management System (ISMS).
* **Security Controls:** The specific safeguards implemented to reduce risk.
    * **Physical:** Fences, CCTV, biometric scanners, security guards.
    * **Technical (Logical):** Firewalls, Multi-Factor Authentication (MFA), Antivirus, Encryption.
    * **Administrative:** Separation of duties, asset classification, security training policies.

---

## 🛡️ NIST Cybersecurity Framework (CSF)
The NIST CSF provides a continuous, lifecycle approach to managing cybersecurity risk across six core functions:

1.  **Govern:** Establishing organizational structures, risk strategies, and leadership commitment.
2.  **Identify:** Mapping out assets, people, and data to understand the attack surface.
3.  **Protect:** Implementing safeguards (policies, tools, training) to prevent breaches.
4.  **Detect:** Utilizing monitoring capabilities (e.g., SIEM tools) to identify active incidents quickly.
5.  **Respond:** Executing procedures to contain, neutralize, and analyze security incidents.
6.  **Recover:** Restoring affected systems from backups and returning to normal operations.

---

## 💻 OWASP Secure Software Principles
Guidelines for building secure applications and avoiding common vulnerabilities:

* **Establish Secure Defaults:** Applications should be highly secure out-of-the-box without requiring user configuration.
* **Fail Securely:** If a system/control fails, it must default to a secure, closed state (e.g., a broken firewall blocks all traffic).
* **Don’t Trust Services:** Never implicitly trust data or security from third-party vendors or external systems; always verify.
* **Avoid Security by Obscurity:** Security should not rely on keeping source code or system architecture a secret. It must rely on strong architecture and cryptography.
* **Defense in Depth:** Using multiple, layered security controls.

---

## 📋 Security Audits & Compliance
A security audit is an independent review of an organization's controls against internal policies and external regulations (laws). 

**The Audit Checklist Lifecycle:**
1.  **Scope Definition:** Identify exactly which assets and systems will be assessed.
2.  **Risk Assessment:** Evaluate risks related to budget, controls, and compliance standards.
3.  **Conduct Audit:** Actively test the identified controls.
4.  **Mitigation Plan:** Create a strategy to fix any discovered vulnerabilities or compliance failures.
5.  **Communicate Results:** Deliver a detailed report to stakeholders outlining findings and required improvements.
