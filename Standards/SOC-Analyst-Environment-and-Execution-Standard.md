# SOC Analyst — Detection, Adversary Tactics & Incident Handling — Environment & Execution Standard

## Purpose

This standard defines where and how the SOC Analyst — Detection, Adversary Tactics & Incident Handling course executes. The full verified enterprise home lab is an intentional part of the curriculum.

It governs system roles, verified infrastructure use, telemetry paths, tool introduction, controlled adversary activity, evidence sources, repository paths, and operational prerequisites. It does not change canonical curriculum numbering, completion state, or the shared locked portfolio README structure.

## Authority Hierarchy

1. Current explicit user instruction
2. Authoritative SOC Analyst — Detection, Adversary Tactics & Incident Handling Curriculum
3. Shared Lab Documentation Standard
4. SOC Analyst Environment & Execution Standard
5. SOC Analyst Course Progress
6. Individual lab

Dedicated home-lab topology, VLAN, virtualization, and live-validation sources remain authoritative for detailed infrastructure state.

## Enterprise Namespace

Current enterprise DNS/FQDN namespace:

`corp.treysecuritylab.com`

Use a host's full FQDN only after its DNS record and connectivity are verified. Do not introduce obsolete `.homelab.arpa` names into new SOC coursework.

## Network Zones

The course may use the verified six-VLAN architecture:

| VLAN | Name | Network | SOC purpose |
| ---: | --- | --- | --- |
| 10 | MANAGEMENT | `10.10.10.0/24` | Administrative control plane |
| 20 | USERS | `10.10.20.0/24` | Enterprise user/end-user telemetry |
| 30 | DMZ | `10.10.30.0/24` | Exposed-service and web investigation zone |
| 40 | SECOPS | `10.10.40.0/24` | SIEM, NSM, DFIR, monitoring, and investigation |
| 50 | SERVERS | `10.10.50.0/24` | AD/DNS, Linux, file, and server workloads |
| 60 | REDTEAM | `10.10.60.0/24` | Controlled adversary simulation and defensive validation |

Do not infer or create additional VLANs unless the user explicitly authorizes an architecture change.

## Core Infrastructure Roles

### OPNsense

Edge firewall/router, Layer-3 gateway, inter-VLAN policy boundary, and source of relevant network/security telemetry when configured and verified.

### SW-Lab-01

Aruba J9774A Layer-2 switching platform for VLAN transport, segmentation, and traffic mirroring when the mirror path is configured and verified.

### ENTHOST-01

Enterprise Proxmox VE virtualization host for server and endpoint workloads after each workload is individually deployed and verified.

### SECHOST-01

Security Proxmox VE virtualization host for SOC/security workloads.

Current implementation note: the SECHOST-01 host, management path, and VLAN 40 transport have been verified. Security VMs, agents, and the passive monitoring path must still be treated according to their live verified state at the time of a lab; do not assume they exist merely because they are in the architecture.

### REDTEAM-01

Dedicated controlled adversary-generation platform on VLAN 60 when connected and verified. It may be used for scanning, enumeration, attack simulation, and defensive-control validation only against authorized lab systems.

## Enterprise Workloads

SOC labs may use systems such as:

- domain controllers / DNS;
- Windows endpoints;
- LINUX-01;
- file services;
- DMZ web services;
- SIEM/security analytics workloads;
- Suricata and Zeek network monitoring;
- Velociraptor / DFIR;
- Microsoft cloud/identity/security services; and
- REDTEAM-01.

No workload is considered operational solely because it appears in the intended architecture. Each lab must verify the required system, network path, time synchronization, data source, agent, collector, sensor, or service before depending on it.

## Tool Education Rule — LOCKED

Every tool must be introduced and taught before the learner is expected to use it independently.

The first substantive use of a tool must explain:

1. What the tool is.
2. Its security purpose.
3. How it works at the level needed for the lab.
4. Where it fits within the home-lab/SOC architecture.
5. Important terminology.
6. Basic operation or navigation.
7. Relevant command, flag, query, filter, or interface syntax.
8. How an analyst interprets the output.
9. What the output can prove and what it cannot prove.

Major platforms may receive dedicated introductory labs.

Instructional progression:

Tool Primer → Guided Orientation → Guided Practice → Operational Verification → Analyst Use Case → Guided Investigation → Evidence Capture → Interpretation → Independent Analyst Task → Later Reuse

Subsequent labs should increasingly use a known tool to accomplish a security objective instead of repeatedly reteaching basic operation.

## SIEM and Security Tooling

The curriculum includes Splunk/SPL as a central SIEM learning platform and Microsoft Sentinel/KQL for Microsoft security operations. The home lab may also retain or use Wazuh where it remains part of the verified infrastructure.

A product name in the curriculum does not mean the product is already installed or operational.

Where applicable, the course can use:

- Splunk;
- Wazuh;
- Suricata;
- Zeek;
- Wireshark/tcpdump;
- Sysmon;
- Windows Event Logs;
- PowerShell logging;
- Velociraptor;
- Microsoft Defender XDR;
- Microsoft Sentinel;
- Nmap;
- Netcat;
- Burp Suite;
- Metasploit;
- Impacket;
- BloodHound;
- Responder;
- password-analysis tools;
- Linux utilities; and
- selected controlled C2 concepts.

The security skill and investigation outcome determine why a tool is used.

## Telemetry Verification Rule

Before an investigation relies on a data source, verify the telemetry chain.

Examples:

Endpoint → Agent/Collector → Network Path → Security Platform → Correct Index/Data Source → Searchable Events

Mirrored Traffic → Switch Mirror/SPAN → Sensor Interface → Suricata/Zeek → Log Output → SIEM/Analyst

Configured is not equivalent to working. Working is not equivalent to receiving data. Receiving data is not equivalent to correctly parsed or useful data.

## Controlled Adversary Activity

Adversary activity must be bounded to systems and networks the user is authorized to test.

Each controlled attack exercise must have a defined defensive purpose such as:

- generating telemetry;
- validating a detection;
- observing artifacts;
- practicing alert triage;
- reconstructing an attack;
- scoping an incident;
- validating containment; or
- improving a detection.

Do not direct controlled course attacks at public/third-party systems.

## Malware Analysis

Malware-analysis exercises must use controlled samples or purpose-built training artifacts in an isolated, non-production environment.

Before execution-based analysis:

- verify isolation;
- verify rollback/recovery capability where applicable;
- define the evidence to collect;
- avoid exposing unrelated networks or credentials; and
- confirm the exercise is required by the lab.

## SOC Lab Evidence Workspaces

Because SOC labs may span multiple operating systems and appliances, each lab must explicitly declare every evidence source before collection.

Default course-specific local workspaces, when needed:

| Platform | Default SOC workspace |
| --- | --- |
| Linux | `~/cyber-labs/soc-lab-XX-<lab-name>/` |
| Windows | `C:\cyber-labs\soc-lab-XX-<lab-name>\` |

Evidence belongs under an `evidence` subdirectory when the platform supports a filesystem workspace.

Tool exports from appliances, SIEMs, or cloud consoles must be staged on an authorized management device, sanitized, checksummed, and tied to the exact lab before publication.

## Screenshot Sources

Follow the shared Lab Documentation Standard:

- Windows: `C:\Pictures\lab-XX-pics`
- Linux: `~/Pictures/lab-XX-pics`

Because Linux and SOC courses reuse lab numbers, the active course must be explicitly identified before screenshots are imported. The updater must validate the target course path and exact filenames before modifying the repository.

## GitHub Paths

Authoritative repository:

`TreySecurityLab/cyber-portfolio`

SOC course path:

`SOC-Analyst/`

Per-lab publication path:

`SOC-Analyst/Module-XX-<Module-Name>/Lab-XX-<Lab-Name>/`

This namespace prevents the SOC Lab 01–77 sequence from colliding with the root-level Linux Lab 01–77 sequence.

## Difficulty Progression

Early labs provide detailed guidance and explicit investigative steps.

Middle labs increasingly require correlation across multiple data sources.

Later labs may present only the initial alert, report, indicator, or scenario and require the learner to determine the investigation path.

This reduction in analytical hand-holding must never reduce:

- lab length/depth;
- tool education when a tool is new;
- command/flag explanations;
- verification checkpoints;
- screenshot requirements;
- evidence integrity;
- documentation quality; or
- reporting requirements.

## Verified-State Rule

Use only operationally verified systems, paths, and telemetry.

If a required component is not operational:

1. stop;
2. identify the missing prerequisite;
3. configure/verify it as an explicit setup task or approved course activity; and
4. only then allow the investigation to depend on it.

Do not document a planned integration as completed.

## Publication Workflow

Linux and Windows native updater/publisher workflows may be used.

When a SOC lab is explicitly complete, ask exactly:

`Which updater do you need: Linux or Windows?`

The updater must validate that it is targeting the **SOC-Analyst** course namespace before repository modification and must fail closed if the course, module, lab, evidence, or screenshot source is ambiguous.

## Change Control

Changes to SOC systems, tool placement, FQDN state, telemetry paths, evidence workspaces, verified infrastructure, or publication behavior belong here.

Changes to SOC lab numbering or titles belong only in the authoritative SOC curriculum. Completion changes belong only in the SOC course-progress file. Portfolio README structure and evidence-presentation rules belong only in the shared Lab Documentation Standard.
