# Phase 1 – Lab Environment Setup

This phase documents the base virtual machines and network configuration.

## Virtual Machines

| VM Name                | OS                  | Purpose                     | RAM/CPU       |
|------------------------|-------------------|-------------------------------|---------------|
| DC                     | Windows Server 2022 | Active Directory Domain
                                                  Controller                 | 2 CPU / 4GB  |
| Win10-Victim           | Windows 10 Pro      | Domain-joined workstation   | 2 CPU / 4GB  |
| Kali-Attacker          | Kali Linux 2023     | Offensive testing           | 2 CPU / 2GB  |
| Splunk-SIEM            | Ubuntu 22.04        | Log collection & analysis   | 2 CPU / 8GB  |


## Network Configuration

- **Hypervisor:** VirtualBox 7
- **Network Type:** Internal Network
- **Network:** 192.168.10.0/24

### IP Addressing

- **Domain Controller (DC):** 192.168.10.7 (Static)
- **Splunk SIEM:** 192.168.10.10 (Static)
- **Kali Attacker:** 192.168.10.250 (Static)
- **Windows 10 Victim:** DHCP (Assigned by DC)


## Notes

- All machines are connected to the same internal network to simulate a corporate LAN.
- Static IPs are assigned for stability.
- Screenshots of VM list and network settings will be added after setup.
