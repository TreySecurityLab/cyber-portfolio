# Cybersecurity Portfolio

This repository documents two structured, hands-on cybersecurity curricula built around verified lab work and portfolio-quality evidence.

## Courses

### Linux Security

A 77-lab Linux-focused progression covering Linux fundamentals, host security, networking, Bash automation, logging, service security, hardening, containers, DFIR, threat hunting, incident response, and final security capstones.

Existing completed Linux labs remain in their current root-level module paths so their Git history, evidence, screenshots, and links are preserved.

### SOC Analyst — Detection, Adversary Tactics & Incident Handling

A separate 77-lab SOC curriculum covering SOC operations, network security monitoring, Windows/Active Directory monitoring, Linux telemetry, SIEM and detection engineering, controlled adversary tactics, endpoint investigation, PowerShell, malware analysis, threat hunting, attack reconstruction, cloud/identity monitoring, and incident handling.

SOC labs are published beneath [`SOC-Analyst/`](SOC-Analyst/) to keep their independent Lab 01–77 numbering separate from the Linux course.

## Lab Environment

The portfolio uses a segmented home-lab environment designed to support enterprise infrastructure, Linux security, SOC monitoring, controlled adversary simulation, virtualization, and incident investigation.

Operational status is evidence-driven: a planned host, VM, agent, sensor, telemetry path, security platform, or cloud integration is not represented as operational until it has been configured and verified.

Current enterprise DNS namespace: `corp.treysecuritylab.com`.

### Network Segmentation

| VLAN | Name | Purpose |
| ---: | --- | --- |
| 10 | MANAGEMENT | Infrastructure administration |
| 20 | USERS | Simulated enterprise endpoints |
| 30 | DMZ | Isolated application/web services |
| 40 | SECOPS | Monitoring, detection, and investigation |
| 50 | SERVERS | Enterprise server infrastructure |
| 60 | REDTEAM | Controlled adversary simulation |

## Linux Security Curriculum

1. [Module 01 — Linux Fundamentals](Module-01-Linux-Fundamentals/)
2. [Module 02 — Linux Security](Module-02-Linux-Security/)
3. Module 03 — Linux Networking & Host Firewalling
4. Module 04 — Bash & Security Automation
5. Module 05 — Linux Logging, Monitoring & Auditing
6. Module 06 — Linux Service & Application Security
7. Module 07 — Linux Hardening & Vulnerability Management
8. Module 08 — Linux Containers & Isolation
9. Module 09 — Linux DFIR & Threat Hunting
10. Module 10 — Linux Incident Response
11. Module 11 — Linux Security Final Capstone

## SOC Analyst Curriculum

See [`SOC-Analyst/`](SOC-Analyst/) for the independent 77-lab **SOC Analyst — Detection, Adversary Tactics & Incident Handling** course.

## Standards and Curriculum Sources

Shared lab documentation rules live under [`Standards/`](Standards/).

Authoritative curricula and progress files are maintained under `Curriculum/` so numbering, scope, and completion state remain explicit and independently controlled.

## Completed Modules

### Linux Security

✅ [Module 01 — Linux Fundamentals](Module-01-Linux-Fundamentals/)

### SOC Analyst — Detection, Adversary Tactics & Incident Handling

No module is complete yet.
