# 🛡️ SIEM & SOAR Architecture Fundamentals

A comprehensive overview of Security Information and Event Management (SIEM) tools, hosting architectures, and dashboard analysis. These notes cover the core infrastructure used by Security Operations Centers (SOCs) to monitor, analyze, and respond to cyber threats in real-time.

---

## 🧠 Core Concepts

### SIEM (Security Information and Event Management)
An application that collects, analyzes, and correlates log data from various sources across an IT infrastructure. 
* **Purpose:** Provides real-time monitoring and tracking of security event logs to identify threats, risks, and vulnerabilities.
* **Limitation:** Currently requires human interaction for the final analysis of security events.

### SOAR (Security Orchestration, Automation, and Response)
A collection of applications, tools, and workflows that use automation to respond to security events.
* **Purpose:** Streamlines the handling of common security incidents, allowing the system to perform mitigation actions without waiting for human intervention. This frees up security analysts to tackle complex threats.

---

## 🏗️ Hosting Architectures

As technology evolves (like the expansion of IoT devices), SIEM tools must scale. Organizations choose their architecture based on resource availability and infrastructure needs:

1. **Self-Hosted:** Operated and maintained entirely by the organization (e.g., *Splunk Enterprise*).
2. **Cloud-Hosted:** Operated by vendors who maintain the infrastructure; accessed via the internet (e.g., *Splunk Cloud*).
3. **Cloud-Native:** Built specifically to leverage cloud computing capabilities like extreme scalability and flexibility (e.g., *Google Chronicle*).

---

## 🔓 Software Licensing Models

| Feature | Open-Source Tools | Proprietary Tools |
| :--- | :--- | :--- |
| **Definition** | Software built collaboratively by the public. | Software developed and owned by a specific company. |
| **Access** | Source code is freely available to modify and improve. | Source code is closed; users pay for usage/training. |
| **Security** | Highly secure due to wide exposure; informed users can patch vulnerabilities immediately. | Users must wait for the owning company to release official updates. |
| **Examples** | **Linux** (OS), **Suricata** (Network Analysis) | **Splunk**, **Google Chronicle** |

---

## 📊 SIEM Tool Spotlights & Dashboards

Different SIEMs offer specialized dashboards to help analysts filter massive amounts of log data efficiently.

### 🟢 Splunk
A leading SIEM offering both Self-Hosted (Enterprise) and Cloud-Hosted (Cloud) solutions to gain full visibility into daily operations.

* **Security Posture:** Displays the last 24 hours of notable events. Used by SOCs to monitor immediate, real-time threats.
* **Executive Summary:** Analyzes overall health over time. Used to provide high-level insights to stakeholders and management.
* **Incident Review:** Highlights high-risk items and provides a visual timeline of events leading up to an incident.
* **Risk Analysis:** Identifies risk for specific objects (users, computers, IPs). Helps prioritize mitigation based on unusual behavior (e.g., logging in at odd hours).

### 🔵 Google SecOps (Chronicle)
A cloud-native SIEM designed to retain, analyze, and search massive datasets based on specific assets, domains, users, or IPs.

* **Enterprise Insights:** Highlights recent alerts (Indicators of Compromise / IOCs) with assigned Confidence Scores and Severity Levels.
* **Data Ingestion & Health:** Monitors the success rate of logs actually reaching the system (ensuring no blind spots).
* **IOC Matches:** Tracks top threats over time to identify trends and direct team focus to the highest priorities.
* **Main Dashboard:** High-level timeline of all security events across all sources to spot broad attack trends.
* **Rule Detections:** Provides statistics on which specific detection rules are triggering the most alerts.
* **User Sign-in Overview:** Tracks access behavior to spot anomalies, like simultaneous logins from impossible geographic locations.

---

## 📖 Glossary of Terms

* **Incident Response:** An organization’s quick attempt to identify an attack, contain the damage, and correct the effects of a breach.
* **Log:** A record of events that occur within an organization’s systems.
* **Metrics:** Key technical attributes (response time, availability) used to assess software performance.
* **Operating System (OS):** The interface between computer hardware and the user (e.g., Linux).
* **Playbook:** A manual providing detailed steps for operational actions.
