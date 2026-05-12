# 🛡️ Google Cybersecurity Course 1: Mega-Cheat Sheet 
**Target Role:** Cloud Security Engineer  
**Strategy:** Concepts are tiered by their daily importance on the job and in interviews.

---

## 🔴 Tier 1: Must Master (The Cloud Security Core)
*These are the concepts you must know inside and out. You will use these daily, and interviewers will test you heavily on them.*

### 1. The CIA Triad (The Core of All Security)
Every security decision relies on balancing these three pillars:
* **Confidentiality:** Keeping secrets safe. Only authorized users can access specific data.
* **Integrity:** Keeping data accurate. Data is authentic, reliable, and hasn't been altered by an attacker.
* **Availability:** Keeping systems running. Authorized users can access the data whenever they need it (e.g., preventing DDoS attacks).

### 2. Scripting, OS, & Databases (Your Daily Tools)
* **Linux:** The open-source operating system that runs most of the cloud. You interact with it primarily via the command-line interface (CLI).
* **Python:** A programming language used to automate repetitive tasks and eliminate human error in security configurations.
* **SQL (Structured Query Language):** The language used to interact with, search, and secure massive databases.

### 3. Core Security Tools (How We Defend)
* **SIEM (Security Information and Event Management):** The "security brain." An application (like Splunk or Google Chronicle) that collects millions of log files and alerts you to real threats.
* **IDS (Intrusion Detection System):** A perimeter alarm. It scans network traffic and alerts the team if it sees unauthorized access or malicious behavior.
* **Network Protocol Analyzer (Packet Sniffer):** A tool (like Wireshark) that captures and dissects the exact data traveling across a network.
* **Antivirus/Anti-malware:** Software that scans device memory to detect, prevent, and eliminate malicious code.

### 4. Cloud-Critical Concepts & Data Privacy
* **Cloud Security:** Ensuring cloud assets are configured correctly and access is strictly limited to authorized users.
* **PII (Personally Identifiable Information):** Any data that can identify a specific person (e.g., Name, Phone number).
* **SPII (Sensitive PII):** Highly restricted personal data (e.g., Social Security Numbers, Credit Card details).
* **Encryption:** Converting readable data (plaintext) into an unreadable secret code (ciphertext) to ensure confidentiality.
* **Web Vulnerability:** A flaw in a website's code (tracked by OWASP) that attackers exploit to steal data or deploy malware.
* **Penetration Testing (Pen Testing):** Legally attacking your own systems to find vulnerabilities before the bad guys do.

### 5. Cloud-Critical Compliance Frameworks
* **FedRAMP:** The gold standard U.S. government program for securing and monitoring Cloud Services.
* **SOC 1 & SOC 2:** Financial and security reports that prove an organization handles user access, privacy, and data safely.

---

## 🟡 Tier 2: Important to Understand (The Interview Vocabulary)
*You don't need to be a master of these, but you must be able to speak intelligently about them during team meetings and interviews.*

### 1. The CISSP 8 Security Domains (How the Industry Works)
1. **Security and Risk Management:** Setting goals, rules, and business continuity plans.
2. **Asset Security:** Protecting and safely destroying physical/digital data.
3. **Security Architecture and Engineering:** Building secure systems and tools.
4. **Communication and Network Security:** Protecting physical networks and Wi-Fi.
5. **Identity and Access Management (IAM):** Controlling *who* has access to *what*.
6. **Security Assessment and Testing:** Running audits to find weaknesses.
7. **Security Operations:** Incident response and active investigations.
8. **Software Development Security:** Writing code securely.

### 2. Social Engineering & Why it Works
*Manipulating humans into breaking security rules.*
* **Phishing:** Tricking users via digital communication.
* **Spear Phishing:** Phishing targeting a *specific* person.
* **Whaling:** Phishing targeting the "big fish" (CEOs/Executives).
* **Vishing:** Voice phishing (phone calls).
* **Smishing:** SMS/Text message phishing.
* **BEC (Business Email Compromise):** Impersonating a boss or vendor to steal money.
* **Social Media Phishing:** Using info scraped from social profiles to craft an attack.
* **Watering Hole Attack:** Infecting a website you know the target frequently visits.
* **Core Principles of Manipulation:** Attackers use Authority, Intimidation, Consensus, Scarcity, Familiarity, Trust, and Urgency to force victims into making quick mistakes.

### 3. Malware (Malicious Software)
* **Virus:** Malicious code that destroys data but *requires a human* to click/open it to execute.
* **Worm:** Self-replicating malware that spreads automatically across networks.
* **Ransomware:** Encrypts an organization's files and demands money for the unlock key.
* **Spyware:** Secretly monitors and steals user data (passwords, locations) without consent.

### 4. Threat Actors & Hackers
* **APTs (Advanced Persistent Threats):** Highly skilled, well-funded (often government) hackers who stay hidden in networks for months.
* **Insider Threats:** Trusted employees or vendors who abuse their access intentionally or accidentally.
* **Hacktivists:** Attackers driven by political or social agendas.
* **The Hacker Types:** * **Ethical (Authorized):** Hired to find bugs legally.
  * **Semi-Authorized:** Finds bugs without permission, but doesn't do damage.
  * **Unethical (Unauthorized):** Breaks the law for financial gain.

### 5. Standard Compliance & Frameworks
* **Framework:** A blueprint of guidelines to mitigate risk. Contains 4 components: Set goals, set guidelines, implement processes, monitor results.
* **Controls:** The actual tools (firewalls, passwords) used to achieve the framework's goals.
* **NIST:** U.S. agency that writes the most respected voluntary cybersecurity frameworks.
* **GDPR:** Strict European data privacy law. Mandates a **72-hour** window to report data breaches.
* **PCI DSS:** The global standard for safely processing Credit Card data.
* **HIPAA:** U.S. law protecting medical records and patient health information (PHI).
* **CIS:** A nonprofit providing actionable, practical defense plans for networks.

### 6. Attack Types & Domains
* **Password Attacks (Comm/Network):** Brute force, Rainbow tables.
* **Supply-Chain Attacks (Multiple Domains):** Infecting a trusted third-party vendor to get to the main target.
* **Cryptographic Attacks (Comm/Network):** Breaking secure communications (Birthday, Downgrade attacks).
* **Adversarial AI (IAM/Network):** Using Machine Learning to make attacks faster and smarter.

---

## 🟢 Tier 3: Just Learn for Knowledge (Context & Trivia)
*Read these to understand the broader context of the field, but do not waste time memorizing them. You will rarely use these in a Cloud Engineering role.*

### 1. Niche Compliance & Terminology
* **FERC-NERC:** Regulations specifically for the North American power grid and electricity companies. 
* **ISO:** General international standards for tech and manufacturing.
* **Technical vs. Transferable Skills:** Technical skills are specific to a tool; transferable skills apply to any job (like communication).

### 2. Historical Events
* **1986:** Brain virus (created by the Alvi brothers).
* **1988:** Morris worm (Robert Morris).
* **2000:** ILOVEYOU virus (Onel de Guzman).
* **2016:** Equifax mega-breach.

### 3. Physical Security & Forensics (Not Cloud-Focused)
* **USB Baiting:** Leaving an infected flash drive in a parking lot hoping an employee plugs it in.
* **Physical Social Engineering:** Tailgating or impersonating the pizza guy to get inside a building.
* **Playbooks:** Step-by-step manuals for responding to incidents.
* **Chain of Custody Playbook:** Documenting exactly who holds physical evidence (hard drives) to present in court.
* **Protecting/Preserving Evidence:** Handling fragile digital data.
* **Order of Volatility:** The rule stating you must secure data that disappears when the power turns off (like RAM) before taking hard drives.

### 4. Ethics of Counterattacks (No "Hacking Back")
* **The Law:** In the U.S. and internationally, counterattacking a hacker is generally illegal and considered vigilantism.
* **The Reason:** Hackers hijack innocent computers. If you counterattack, you are likely destroying an innocent person's machine or risking international war (if state-sponsored). 
* **The Exception:** Only military or approved federal agents are legally allowed to counterattack.
this?
