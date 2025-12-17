# Lab Setup — Blue Team Environment

This document describes the initial setup of my local Blue Team lab environment.

---

## Host Machine
- OS: Windows
- Virtualization: VMware Workstation Player
- Purpose: Local lab for Defensive Cybersecurity (SOC / Blue Team)

---

## Virtual Machines Overview

### VM 1 — Ubuntu Server (Manager)
- VM Name: ubuntu-blue-team
- OS: Ubuntu Server 24.04 LTS
- Role: Log manager / future Wazuh & SIEM manager
- CPU: 1 processor / 2 cores (2 vCPU)
- RAM: 4 GB
- Disk: 40 GB
- Network: NAT
- Interface: CLI-only (no GUI)
- Snapshot: clean-install

**Notes:**
- Fresh installation
- No security tools installed
- Used as baseline for future SIEM deployment

---

### VM 2 — Windows Endpoint
- VM Name: win10-lab
- OS: Windows 10 x64
- Role: Monitored endpoint (logs, Sysmon, agent)
- CPU: 1 processor / 2 cores (2 vCPU)
- RAM: 4 GB
- Disk: 60 GB
- Network: NAT
- Snapshot: clean-install

**Notes:**
- Local user account created
- Windows Update completed
- Event Viewer and PowerShell validated

---

## Snapshot Strategy
- `clean-install`: Fresh OS installation before any security tooling

Snapshots are taken before:
- Installing Sysmon
- Installing Wazuh agent
- Simulating attacks
- Performing incident response exercises

---

## Next Steps
- Validate connectivity between VMs
- Begin Project 00 — Fundamentals
