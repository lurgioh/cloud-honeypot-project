# 🌐 Cloud Honeypot Lab — T-Pot on DigitalOcean

A cloud-hosted honeypot deployed using **T-Pot**, designed to safely capture and analyze real-world attacker behavior including SSH brute-force attempts, botnet activity, malware download attempts, and automated network scanning.

This project showcases the deployment, configuration, and monitoring of a **public-facing honeypot** for cybersecurity learning and threat intelligence collection.

---

## 🚀 Overview

**Platform:** DigitalOcean  
**Environment:** Ubuntu (T-Pot Installer)  
**Purpose:** Capture and analyze active internet attacks in a controlled, isolated cloud environment.

T-Pot is a multi-honeypot framework bundling:
- Cowrie (SSH/Telnet)
- Dionaea (malware collection)
- Suricata (IDS)
- Honeytrap (port interaction)
- Elastic Stack (Elasticsearch + Kibana)
- CyberChef (analysis)
- Spiderfoot (OSINT)
- Multiple network decoys & sensors

---

## 🧱 Architecture

```text
Internet
   │
   ▼
DigitalOcean Droplet (Public IP)
   │
   └── T-Pot Honeypot Stack (Docker)
         ├── Cowrie (SSH / Telnet honeypot)
         ├── Dionaea (malware capture)
         ├── Suricata (intrusion detection)
         ├── Honeytrap (service emulation)
         ├── Elasticsearch (log storage)
         └── Kibana (log analysis dashboards)
