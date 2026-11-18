# Acme Corp Purple-Team Lab

A self-built Active Directory + SIEM home lab, created for an independent, authorized purple-team exercise. The goal is to simulate a small company network, attack it as a penetration tester, then detect and respond to that attack as a SOC analyst — producing a professional pentest report and a SOC detection write-up as portfolio deliverables.

## Status

- [x] **Build phase** — AD domain, Domain Controller, 2 workstations, Wazuh SIEM, Sysmon logging. [Full build documentation](docs/Acme-Corp-Build-Documentation.docx)
- [x] **Attack phase** — Kerberoasting, weak-password Domain Admin compromise, full NTDS.dit dump. [Penetration Test Report](docs/Acme-Corp-Pentest-Report.docx)
- [x] **Detection phase** — SIEM hunt, detection gap analysis, custom Sigma/Wazuh rule. [SOC Detection & Incident Report](docs/Acme-Corp-SOC-Detection-Report.docx)
- [ ] **Hardening & final report** — pending

## Environment

| Host | Role | OS | IP |
|---|---|---|---|
| DC01-AcmeCorp | Domain Controller / DNS | Windows Server 2022 | 192.168.229.10 |
| WKS01-Ali | IT Workstation | Windows 11 Enterprise | 192.168.229.20 |
| WKS02-Sara | HR Workstation | Windows 11 Enterprise | 192.168.229.21 |
| Ubuntu24-SIEM | Wazuh Manager/Indexer/Dashboard | Ubuntu 24.04 LTS | 192.168.229.30 |
| Kali | Attacker platform | Kali Linux | 192.168.229.100 |

All hosts run on an isolated VMware host-only network (VMnet2, 192.168.229.0/24) with no internet access.

## Tools

VMware Workstation · Windows Server 2022 · Windows 11 Enterprise · Ubuntu 24.04 · Wazuh 4.14 · Sysmon (SwiftOnSecurity config) · Kali Linux

## Repo structure

- `docs/` — Build documentation, Penetration Test Report, SOC Detection & Incident Report
- `diagrams/` — Network topology diagram
- `screenshots/` — Supporting evidence screenshots

## Disclaimer

This is a fully isolated, self-owned lab environment. No real systems, networks, or third parties were involved or tested.
