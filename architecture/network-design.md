# Lab Architecture

This lab simulates a small Active Directory environment for attack and detection exercises.

## Components

1. **Kali Linux (Attacker)**  
   - Offensive machine used to simulate attacks.
   - Tools installed: Nmap, CrackMapExec, Mimikatz, etc.

2. **Windows 10 (Victim)**  
   - Domain-joined workstation.
   - Logs forwarded to Splunk.
   - Simulates normal user activity.

3. **Windows Server (Domain Controller / AD)**  
   - Runs Active Directory and DNS.
   - Hosts user accounts, groups, and organizational units (OUs).

4. **Ubuntu Server (Splunk SIEM)**  
   - Collects and analyzes logs from the DC and Windows 10.
   - Hosts dashboards and alerts for detection.

## Network Flow

- Kali attacks the Windows 10 workstation over the internal network.
- Windows 10 communicates with the Domain Controller for authentication.
- Logs from both the DC and Windows 10 are forwarded to Splunk for monitoring.
