# Active Directory Home Lab – Attack Simulation & Detection Engineering

This repository documents a **production-style Active Directory home lab** designed to simulate real-world enterprise attacks and demonstrate **security monitoring, detection engineering, and SIEM analysis** using Splunk.

The lab replicates a small corporate Windows environment and showcases:
- Adversary tradecraft against Active Directory
- Windows telemetry collection and analysis
- Detection logic mapped to attacker behavior
- SOC-style investigation workflows

This project is intended to demonstrate **hands-on defensive security skills** relevant to SOC, Blue Team, and Detection Engineering roles.

---

## 🏗️ Environment Overview

The lab consists of the following components:

- **Windows Server Domain Controller**
  - Active Directory Domain Services
  - DNS
  - Domain users and groups

- **Windows 10 Workstation**
  - Domain-joined endpoint
  - Enhanced security logging enabled

- **Splunk Enterprise (SIEM)**
  - Centralized log ingestion
  - Detection searches and alerts
  - Dashboards for security visibility

- **Kali Linux**
  - Attack platform used to simulate adversary behavior

All attack activity is performed against the lab environment, with detections validated in Splunk.

---

## 🧩 Architecture

A detailed architecture diagram and component breakdown are available in:

- 📊 `architecture/lab-diagram.png`
- 📄 `architecture/design.md`

---

## 📁 Repository Structure

```text
ad-home-lab/
│
├── README.md                 ← Project overview
│
├── architecture/             ← Architecture diagrams and design notes
│
├── setup/                    ← Environment build documentation
│   ├── 01-environment/       ← Virtual machine creation
│   ├── 02-splunk/            ← Splunk installation & configuration
│   ├── 03-active-directory/  ← Domain services & identity setup
│   ├── 04-windows10/         ← Endpoint configuration & logging
│   └── 05-kali/              ← Attacker tooling and access
│
├── attacks/                  ← Attack execution and validation
│
├── detection/                ← Splunk searches and alerts
│
├── dashboards/               ← Security dashboards
│
├── screenshots/              ← Visual evidence of setup, attacks, and detections
