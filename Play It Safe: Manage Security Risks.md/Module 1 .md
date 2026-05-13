# 🛡️ Module 1 — Foundations of Cybersecurity & Risk Management

> **Google Cybersecurity Certificate** | Study Notes + Revision Guide  
> By Darshan | Cloud Security Engineer Roadmap 🚀

---

## 📋 Table of Contents

- [Key Vocabulary](#-key-vocabulary)
- [Risk Management Overview](#-risk-management-overview)
- [Threats, Risks & Vulnerabilities](#-threats-risks--vulnerabilities)
- [NIST RMF — 7 Steps](#-nist-rmf--7-steps)
- [8 CISSP Security Domains](#-8-cissp-security-domains)
- [Important Formulas & Mental Models](#-important-formulas--mental-models)
- [Exam Tips](#-exam-tips)

---

## 📖 Key Vocabulary

| Term | Definition |
|------|-----------|
| **Asset** | Anything of value to an organization (digital or physical) |
| **Risk** | Anything that can impact the **confidentiality, integrity, or availability (CIA)** of an asset |
| **Threat** | Any circumstance or event that can negatively impact assets |
| **Vulnerability** | A weakness that can be exploited by a threat |
| **Security Posture** | An organization's ability to manage defense of critical assets AND react to change |
| **Ransomware** | Malicious attack where threat actors **encrypt data** and demand payment to restore access |
| **Social Engineering** | Manipulation technique that exploits **human error** to gain private information or access |
| **Business Continuity** | Organization's ability to maintain productivity by establishing **risk disaster recovery plans** |
| **Shared Responsibility** | All individuals within an org take an active role in **lowering risk** and maintaining security |
| **Risk Mitigation** | Having the right procedures and rules in place to **quickly reduce** the impact of a risk |
| **Internal Threat** | Current/former employee, vendor, or partner who poses a security risk |
| **External Threat** | Anything **outside** the organization that can harm organizational assets |

---

## 🎯 Risk Management Overview

### What Are Assets?

**Digital assets:**
- Social Security Numbers (SSNs)
- Dates of birth
- Bank account numbers
- Mailing addresses

**Physical assets:**
- Payment kiosks
- Servers
- Desktop computers
- Office spaces

---

### 4 Risk Management Strategies

```
┌─────────────────────────────────────────────────────────────┐
│                    RISK STRATEGIES                          │
├──────────────┬──────────────────────────────────────────────┤
│ Acceptance   │ Accept the risk to avoid disrupting business │
│              │ continuity (low-impact risks)                │
├──────────────┼──────────────────────────────────────────────┤
│ Avoidance    │ Create a plan to avoid the risk altogether   │
├──────────────┼──────────────────────────────────────────────┤
│ Transference │ Transfer risk to a third party (e.g. cyber   │
│              │ insurance, outsourcing)                      │
├──────────────┼──────────────────────────────────────────────┤
│ Mitigation   │ Lessen the impact of a known risk            │
└──────────────┴──────────────────────────────────────────────┘
```

> 💡 **Real-world example:** A company can't afford to fix every vulnerability right now — they *accept* low-severity bugs while *mitigating* critical ones. This is standard triage.

---

## ⚠️ Threats, Risks & Vulnerabilities

### Common Threat Types

| Threat | Description |
|--------|-------------|
| **Insider Threats** | Employees/vendors abuse authorized access to harm the org |
| **Advanced Persistent Threats (APTs)** | Threat actor maintains **unauthorized access for extended time** — stealthy, long-game attacks |

### Risk Factors That Increase Likelihood

1. **External Risk** — Threat actors trying to access private info from outside
2. **Internal Risk** — Employees, vendors, or partners going rogue
3. **Legacy Systems** — Old, unpatched systems (e.g., old vending machines on the network!) still creating attack surface
4. **Multiparty Risk** — Third-party vendors with access to your IP and trade secrets
5. **Software Compliance/Licensing** — Unpatched or non-compliant software

> ⚡ **My important note:** Legacy systems are massively underestimated in the real world. In cloud security, you'll often find forgotten EC2 instances or old servers still running — these are goldmines for attackers.

### Key Resources to Know
- **NIST** — publishes cybersecurity risk lists
- **OWASP Top 10** — top 10 most critical security risks to **web applications**, updated regularly

---

## 🔄 NIST RMF — 7 Steps

The **National Institute of Standards and Technology Risk Management Framework** is a structured process for managing security and privacy risks.

```
Step 1 → PREPARE
Step 2 → CATEGORIZE
Step 3 → SELECT
Step 4 → IMPLEMENT
Step 5 → ASSESS
Step 6 → AUTHORIZE
Step 7 → MONITOR
```

### Detailed Breakdown

| # | Step | What It Means |
|---|------|--------------|
| 1 | **Prepare** | Activities necessary to manage security & privacy risks **before** a breach occurs |
| 2 | **Categorize** | Develop risk management processes and tasks; classify systems by impact level |
| 3 | **Select** | Choose, customize, and **document controls** that protect the organization |
| 4 | **Implement** | Actually put the security and privacy plans into action |
| 5 | **Assess** | Determine if controls are **implemented correctly** and producing desired outcomes |
| 6 | **Authorize** | Be **accountable** for the security and privacy risks that may exist — a senior official signs off |
| 7 | **Monitor** | Continuously be aware of how systems are operating; ongoing awareness |

> ⚡ **Memory trick:** **P-C-S-I-A-A-M** → "**Please Create Secure Infrastructure And Always Monitor**"

> 💡 **Important:** The NIST RMF is **not one-and-done**. It's a cycle. After Monitor, you feed information back into Prepare and repeat. This is why cloud environments use continuous monitoring tools like AWS Security Hub or Azure Defender.

---

## 🏛️ 8 CISSP Security Domains

These are the core knowledge areas that define cybersecurity as a profession. As a cloud security engineer, domains 1, 3, 4, and 5 will be your bread and butter.

---

### Domain 1 — Security & Risk Management

**Core focus:** Establishing the organization's overall security posture.

Includes:
- Security goals & objectives
- Risk mitigation processes
- Compliance (legal regulations)
- Business continuity plans
- Professional and organizational ethics
- **InfoSec** (processes established to secure information)

InfoSec design areas:
- Incident response
- Vulnerability management
- Application security
- **Cloud security** ← directly relevant to your career
- Infrastructure security

> 💡 **Real example:** If a company needs to comply with **GDPR** (EU's General Data Protection Regulation), they must alter how they handle PII — that falls under this domain.

---

### Domain 2 — Asset Security

**Core focus:** Managing cybersecurity processes around organizational assets — storage, maintenance, retention, and **destruction** of physical and virtual data.

Key tasks:
- Security impact analysis
- Recovery plan establishment
- Managing data exposure based on risk level
- Creating **backups** to restore environment after incidents

> ⚡ **Important:** Destruction of data matters as much as storage. If you don't properly wipe decommissioned servers, attackers can recover data. In cloud, this means proper **volume deletion and snapshot management**.

---

### Domain 3 — Security Architecture & Engineering

**Core focus:** Managing data security through effective tools, systems, and processes.

Key design principles (memorize these):

| Principle | Meaning |
|-----------|---------|
| **Threat Modeling** | Proactively identify and address threats during design phase |
| **Least Privilege** | Only give the minimal access needed to do the job |
| **Defense in Depth** | Multiple layers of security controls — one layer failing ≠ total compromise |
| **Fail Securely** | When a system fails, it should default to a **secure state**, not open |
| **Separation of Duties** | No single person has enough access to cause undetected harm |
| **Keep It Simple** | Complex systems = more attack surface; simpler is more secure |
| **Zero Trust** | Trust **no one** by default — verify everything, every time |
| **Trust but Verify** | Even trusted entities should be verified |

**Tools used:** SIEM (Security Information and Event Management) — monitors for flags like unusual login activity.

> ⚡ **Zero Trust** is the current industry standard for cloud security architecture. AWS, Azure, Google Cloud all push ZTA heavily. Learn this deeply.

---

### Domain 4 — Communication & Network Security

**Core focus:** Managing and securing physical networks and wireless communications — on-site, remote, and cloud.

Key challenge: Remote/hybrid work environments where employees access networks outside the main office.

Solutions:
- Restricted network access controls
- Secure remote access (VPNs, Zero Trust Network Access)

> 💡 **Cloud relevance:** In AWS/GCP/Azure, this maps to VPC design, security groups, NACLs, and private endpoints. Network security is foundational cloud security.

---

### Domain 5 — Identity & Access Management (IAM)

**Core focus:** Ensuring user identities are **trusted, authenticated**, and that access to assets is **authorized**.

Key concept: **Principle of Least Privilege** — grant only the minimal access and authorization required to complete a task.

> **Example:** A customer service rep should only see a customer's phone number while resolving an issue — not their full financial data. Access gets removed once the issue is resolved.

> ⚡ **This is arguably the most critical domain for Cloud Security.** AWS IAM, Azure AD, Google IAM — misconfigurations here cause the majority of real cloud breaches. Capital One breach (2019) was an IAM misconfiguration. Study this deeply.

---

### Domain 6 — Security Assessment & Testing

**Core focus:** Identifying and mitigating risks, threats, and vulnerabilities through systematic testing.

Key activities:
- **Penetration Testing (Pen Testing)** — ethical hackers find vulnerabilities before real attackers do
- Security control testing
- Data collection and analysis
- **Security audits** — reduce probability of data breach
- Auditing user permissions

> 💡 This domain is where the fun is if you're drawn to offensive security / pen testing. But for cloud security engineers, you'll be doing more defensive assessment — cloud configuration reviews, misconfig scanning (CSPM tools like Wiz, Orca, Prisma Cloud).

---

### Domain 7 — Security Operations

**Core focus:** Investigation of potential data breaches and implementing preventative measures after incidents.

Tools and strategies:
- Training and awareness
- Reporting and documentation
- Intrusion detection and prevention (IDS/IPS)
- **SIEM tools**
- Log management
- Incident management
- **Playbooks** (step-by-step response guides)
- Post-breach forensics
- Lessons learned reviews

> ⚡ **Detection Engineering** (building detection rules in SIEM) is one of the hottest skills in 2025-2026. If you want to specialize, this + cloud = very employable.

---

### Domain 8 — Software Development Security

**Core focus:** Using secure programming practices and guidelines to create secure applications.

Key principle: **Security must be in every phase of the SDLC**, not bolted on at the end.

SDLC phases where security applies:
- Design → Threat modeling
- Development → Secure coding practices
- Testing → Application security testing, pen testing
- Release → Compliance verification

**Roles involved:**
- Quality assurance professionals
- Pen testers
- Security engineers

> 💡 **Example from the module:** An analyst at a pharmaceutical company must ensure encryption is properly configured for a new medical device storing patient data. That's Domain 8 + Domain 3 overlap.

> ⚡ **DevSecOps** is the modern implementation of this domain — integrating security into CI/CD pipelines. Relevant to your roadmap if you move toward cloud security engineering with a dev component.

---

## 🔢 Important Formulas & Mental Models

### Risk Formula
```
Risk = Likelihood of a Threat × Impact
```

**Analogy:** Risk = being late to work. Threats = traffic, flat tire, accident. The higher the likelihood of those events AND the greater the impact (missing an important meeting), the higher the risk.

### CIA Triad (Foundational — Everything References This)
```
┌─────────────────────────────────────────┐
│              CIA TRIAD                  │
│                                         │
│   C — Confidentiality                   │
│       Only authorized people see data   │
│                                         │
│   I — Integrity                         │
│       Data is accurate and unaltered    │
│                                         │
│   A — Availability                      │
│       Data is accessible when needed   │
└─────────────────────────────────────────┘
```

Every security control, policy, and risk assessment ultimately ties back to protecting one or more of these three properties.

---

## 🎯 Exam Tips

1. **NIST RMF order matters** — P-C-S-I-A-A-M. Don't confuse Assess (step 5) and Authorize (step 6).
2. **Authorize = accountability** — it's when a senior official accepts the remaining risk and takes ownership.
3. **Least Privilege** appears in Domain 3 AND Domain 5 — same concept, applied in design (Domain 3) and operations (Domain 5).
4. **Shared Responsibility** is a Domain 3 concept — everyone in the org contributes to security during system design.
5. **Social engineering exploits humans, not systems** — it's a people problem, not a technology problem.
6. **APTs are about persistence** — the threat actor's goal is to stay undetected for as long as possible.
7. **OWASP Top 10 = web application risks** — don't confuse with general risk frameworks.
8. **Business continuity** is about keeping the business running during/after an incident — it's proactive planning.

---

## 🔗 Resources

- [NIST RMF Official Documentation](https://csrc.nist.gov/projects/risk-management)
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)
- [GDPR Overview](https://gdpr.eu/)

---

> **Next:** Module 2 — Network Security Fundamentals  
> **Status:** ✅ Module 1 Complete

---

*Notes compiled during Google Cybersecurity Certificate — Phase 1 of Cloud Security Engineer Roadmap 2025–2030*
