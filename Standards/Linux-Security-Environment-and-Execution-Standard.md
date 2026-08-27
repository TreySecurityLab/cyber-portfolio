# Linux Security — Environment & Execution Standard

## Purpose

This standard defines where and how new Linux Security labs execute. It controls Linux execution systems, verified infrastructure integration, local paths, evidence sources, repository workflows, and operational prerequisites. It does not change the authoritative curriculum, completion state, or shared locked portfolio README format.

## Authority Hierarchy

1. Current explicit user instruction
2. Authoritative Linux Security Curriculum
3. Shared Lab Documentation Standard
4. Linux Security Environment & Execution Standard
5. Linux Security Course Progress
6. Individual lab

Dedicated authoritative home-lab topology/VLAN sources govern detailed infrastructure state. If authorities conflict, stop and surface the discrepancy instead of guessing.

## Historical Preservation

Completed historical Linux labs retain their original execution environments, evidence, screenshots, and Git history unless the user explicitly authorizes a factual correction.

The current standard governs newly generated work, including unfinished Lab 11 and future Linux labs.

## Primary Linux Target

### LINUX-01

- Primary Ubuntu Server security target.
- Hosted on ENTHOST-01.
- Network placement: VLAN 50 — SERVERS.
- Verified address baseline: `10.10.50.40/24`.
- Default gateway baseline: `10.10.50.1`.
- Course lab user: `testlab`.
- Linux lab root: `~/cyber-labs`.
- Per-lab workspace: `/home/testlab/cyber-labs/lab-XX-<lab-name>`.
- Per-lab evidence: `/home/testlab/cyber-labs/lab-XX-<lab-name>/evidence`.

Current enterprise DNS namespace: `corp.treysecuritylab.com`.

Use `linux-01.corp.treysecuritylab.com` only when that FQDN is verified in the active environment. Do not fall back to obsolete `.homelab.arpa` naming in newly generated work.

## Supporting Infrastructure

The Linux course may use verified portions of:

- ENTHOST-01 / Proxmox VE;
- OPNsense;
- SW-Lab-01;
- VLAN 10 MANAGEMENT;
- VLAN 40 SECOPS;
- VLAN 50 SERVERS;
- VLAN 60 REDTEAM;
- authorized management systems;
- REDTEAM-01 for controlled remote validation; and
- security tooling when it meaningfully supports a Linux objective.

Infrastructure must improve realism, validation, troubleshooting, evidence, or defensive understanding. It must not replace the canonical Linux lesson.

## Network Baseline

Current VLAN scope is limited to:

| VLAN | Name | Network | Purpose |
| ---: | --- | --- | --- |
| 10 | MANAGEMENT | `10.10.10.0/24` | Administrative control plane |
| 20 | USERS | `10.10.20.0/24` | Simulated user endpoints |
| 30 | DMZ | `10.10.30.0/24` | Isolated application services |
| 40 | SECOPS | `10.10.40.0/24` | Monitoring, detection, and investigation |
| 50 | SERVERS | `10.10.50.0/24` | Enterprise servers including LINUX-01 |
| 60 | REDTEAM | `10.10.60.0/24` | Controlled adversary activity |

Do not infer additional VLANs or stale physical-port assignments. Detailed switch-port and tagging state must follow the current verified home-lab source.

## Linux Objective Protection

Examples:

- SSH labs primarily teach SSH security even when firewall or VLAN controls provide defense in depth.
- Auditd labs primarily teach Linux auditing even when events are later forwarded to a SIEM.
- Networking labs teach Linux networking, sockets, packet capture, routing, DNS, and host firewall behavior from the Linux system perspective.
- DFIR and incident-response labs remain Linux-centered even when another system generates controlled activity.

## Tool Introduction

When a major Linux utility or platform is first introduced, teach what it is, why it is used, how it works at the level needed, core terminology, basic operation, output interpretation, and every command/flag used before expecting independent operation.

## Verified-State Rule

Use only verified operational infrastructure.

A host, VM, FQDN, VLAN placement, switch-port assignment, route, firewall rule, sensor, monitoring integration, repository path, or evidence source must be verified before a lab depends on it.

Planned components may be described as future opportunities but must not be represented as operational.

## Evidence Retrieval

Default Linux evidence source for applicable labs:

- Host: `10.10.50.40`
- User: `testlab`
- Path: `/home/testlab/cyber-labs/lab-XX-<lab-name>/evidence`

Updater scripts must retain a lab-specific host override and a source override. Evidence may be retrieved by SSH/SCP from any authorized management device.

Do not automatically fall back to an unverified hostname, IP, path, or source.

## Repository Paths

Authoritative repository: `TreySecurityLab/cyber-portfolio`

Linux course GitHub paths remain root-level to preserve completed-lab history:

`Module-XX-<Module-Name>/Lab-XX-<Lab-Name>/`

Verified local repository conventions:

| Platform | Repository path |
| --- | --- |
| Linux | `~/cyber-portfolio` when verified on that device |
| Windows | `C:\cyber-portfolio\` |
| Other | Use the path explicitly verified in the active session |

## Screenshot Sources

Follow the shared Lab Documentation Standard:

- Windows: `C:\Pictures\lab-XX-pics`
- Linux: `~/Pictures/lab-XX-pics`

## Publication Workflow

Linux and Windows native updater/publisher workflows remain supported.

When a lab is explicitly complete, ask exactly:

`Which updater do you need: Linux or Windows?`

Generate only the requested updater unless the user explicitly asks for both.

The updater must validate that it is publishing the **Linux Security** lab and the exact root-level Linux module path before repository modification.

## Change Control

Changes to Linux execution systems, paths, current FQDN state, host roles, verified network placement, evidence retrieval, or publication behavior belong here.

Changes to Linux lab numbering/titles belong only in the authoritative Linux curriculum. Completion-state changes belong only in the Linux progress file. README structure and evidence-presentation rules belong only in the shared Lab Documentation Standard.
