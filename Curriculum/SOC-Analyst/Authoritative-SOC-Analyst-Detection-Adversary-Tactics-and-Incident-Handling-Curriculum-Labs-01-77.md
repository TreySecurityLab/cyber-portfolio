# SOC Analyst — Detection, Adversary Tactics & Incident Handling — Authoritative Curriculum Labs 01–77

This file is the authoritative curriculum for this course.

## Authority Rule

Never infer, reorder, insert, delete, replace, shift, rename, or renumber labs. Never allow an old chat, Git commit, directory, README, script, memory, or prior assistant response to override this curriculum.

Before generating a new lab, verify its canonical lab number, title, module, and completion state against this file and the matching course-progress file.

If an authoritative source conflicts with this curriculum, stop and surface the discrepancy instead of guessing or silently changing anything.

Only the user may authorize curriculum, module, title, or numbering changes.

## Purpose

Develop job-relevant SOC analyst capability across telemetry, detection, alert triage, network and endpoint investigation, SIEM, adversary behavior, PowerShell investigation, malware analysis, threat hunting, attack reconstruction, cloud/identity monitoring, incident handling, and professional reporting.

## Program Structure

- 77 canonical labs.
- 11 modules.
- 7 labs per module.
- Each module ends with a capstone or integrated final exercise.
- Lab documentation, evidence, screenshots, verification, and publication must follow the shared locked Lab Documentation Standard.
- Operational execution must follow this course's dedicated Environment & Execution Standard.

## Course Rules

- The course is independently designed from general cybersecurity concepts, public standards/frameworks, official vendor documentation, the verified home-lab architecture, and user-provided sources.
- The full enterprise home lab may be used when the required systems, VLAN paths, telemetry sources, and tools are operationally verified.
- Controlled adversary activity exists to teach detection, investigation, threat hunting, validation, and incident handling; it is not performed against unauthorized external systems.
- Tools are taught before independent use. The first substantive use of a tool must explain what it is, its security purpose, how it works, where it fits in the lab architecture, important terminology, basic operation, and how analysts interpret its output.
- Major platforms may receive dedicated introductory labs. Later labs increasingly measure the security capability demonstrated with the tool instead of repeatedly teaching basic navigation.
- Later investigations reduce analytical hand-holding while retaining the same lab length, walkthrough depth, evidence burden, verification checkpoints, screenshot requirements, and documentation quality.
- Malware-analysis exercises must remain controlled, isolated, and appropriate for a non-production training environment.

---

## Module 01 — SOC Foundations

SOC roles, analyst workflow, telemetry, alert triage, prioritization, documentation, and escalation.

### Lab 01
Security Operations Center Fundamentals

### Lab 02
Security Telemetry & Data Sources

### Lab 03
Events, Alerts & Incidents

### Lab 04
Alert Triage Fundamentals

### Lab 05
Severity, Priority & Risk Assessment

### Lab 06
SOC Case Documentation & Escalation

### Lab 07
SOC Foundations Capstone

---

## Module 02 — Network Security Monitoring

Network telemetry, protocol analysis, packet capture, IDS/NSM concepts, and defensive traffic investigation.

### Lab 08
TCP/IP for SOC Analysts

### Lab 09
DNS Security Investigation

### Lab 10
HTTP & HTTPS Investigation

### Lab 11
DHCP, ARP & ICMP Analysis

### Lab 12
Packet Capture & Traffic Investigation

### Lab 13
Suricata & Zeek Network Monitoring

### Lab 14
Network Security Investigation Capstone

---

## Module 03 — Windows & Active Directory Security Monitoring

Windows and Active Directory security telemetry, authentication, PowerShell, persistence, and endpoint investigation.

### Lab 15
Windows Event Log Investigation

### Lab 16
Sysmon Endpoint Telemetry

### Lab 17
Active Directory Authentication Monitoring

### Lab 18
Account & Logon Investigation

### Lab 19
PowerShell Security Monitoring

### Lab 20
Windows Persistence Detection

### Lab 21
Windows & Active Directory Investigation Capstone

---

## Module 04 — Linux Security Monitoring

Linux telemetry and investigations from the SOC analyst perspective without duplicating Linux administration coursework.

### Lab 22
Linux Log Investigation

### Lab 23
Linux Authentication Monitoring

### Lab 24
Auditd Security Event Analysis

### Lab 25
SSH Attack Detection

### Lab 26
Sudo, Account & Privilege Monitoring

### Lab 27
Linux Persistence & IOC Investigation

### Lab 28
Linux SOC Investigation Capstone

---

## Module 05 — SIEM & Detection Engineering

SIEM architecture, data onboarding, SPL, correlation, monitoring, detection logic, alerting, and tuning.

### Lab 29
Splunk Architecture for SOC Operations

### Lab 30
Security Log Onboarding & Normalization

### Lab 31
SPL Search & Investigation Fundamentals

### Lab 32
Event Correlation & Timeline Analysis

### Lab 33
SOC Dashboards & Monitoring Views

### Lab 34
Detection Rules, Alerting & Tuning

### Lab 35
SIEM & Detection Engineering Capstone

---

## Module 06 — Adversary Tactics & Hacker Tools

Controlled adversary behavior used to understand attack evidence, detection opportunities, and incident-handling decisions.

### Lab 36
Reconnaissance & Enumeration

### Lab 37
Network Scanning & Service Discovery

### Lab 38
Credential Attacks & Password Analysis

### Lab 39
Windows / Active Directory Adversary Techniques

### Lab 40
Exploitation & Controlled Attack Validation

### Lab 41
Lateral Movement, Pivoting & C2 Concepts

### Lab 42
Adversary Tactics Capstone

---

## Module 07 — Endpoint Investigation, PowerShell & Malware Analysis

Endpoint triage, PowerShell investigation, forensic artifacts, malware analysis, and DFIR workflows.

### Lab 43
Endpoint Detection & Response Fundamentals

### Lab 44
Velociraptor Collection & Endpoint Triage

### Lab 45
PowerShell Investigation Techniques

### Lab 46
Process, File & Registry Artifact Analysis

### Lab 47
Malware Static Analysis Fundamentals

### Lab 48
Malware Behavioral Analysis

### Lab 49
Endpoint & Malware Investigation Capstone

---

## Module 08 — Threat Hunting & Attack Reconstruction

Threat hunting, IOC analysis, timeline development, ATT&CK mapping, root-cause analysis, and detection validation.

### Lab 50
Indicator Analysis & Enrichment

### Lab 51
MITRE ATT&CK Mapping

### Lab 52
Hypothesis-Driven Threat Hunting

### Lab 53
Enterprise IOC Sweeping

### Lab 54
Incident Timeline Development

### Lab 55
Attack Reconstruction & Root-Cause Analysis

### Lab 56
Threat Hunting & Detection Validation Capstone

---

## Module 09 — Cloud, Identity & Microsoft Security Operations

Identity and cloud security monitoring, Defender XDR, Azure security telemetry, Sentinel, and KQL.

### Lab 57
Microsoft Entra ID Security Monitoring

### Lab 58
Cloud Authentication & Sign-In Investigation

### Lab 59
Microsoft Defender XDR Investigation

### Lab 60
Identity Threat Detection

### Lab 61
Azure Activity & Security Log Investigation

### Lab 62
Microsoft Sentinel & KQL

### Lab 63
Cloud & Identity Investigation Capstone

---

## Module 10 — Incident Handling & Response

End-to-end incident handling from readiness and identification through recovery, validation, reporting, and lessons learned.

### Lab 64
Incident Response Preparation & Readiness

### Lab 65
Incident Identification, Scope & Impact

### Lab 66
Containment Decision Making

### Lab 67
Evidence Preservation & Investigation Records

### Lab 68
Eradication, Recovery & Validation

### Lab 69
Incident Reporting & Lessons Learned

### Lab 70
Incident Handling Capstone

---

## Module 11 — Enterprise SOC Final Capstone

Integrated enterprise SOC operations, adversary simulation, detection, investigation, hunting, containment, recovery, and reporting.

### Lab 71
Build the Enterprise SOC Monitoring Environment

### Lab 72
Generate Controlled Adversary Activity

### Lab 73
Detect & Triage the Attack

### Lab 74
Investigate & Correlate the Incident

### Lab 75
Threat Hunt, Scope & Contain

### Lab 76
Recover, Validate & Complete Incident Assessment

### Lab 77
Professional SOC Analyst Portfolio Presentation

---
