# Lab Documentation Standard — LOCKED

## Purpose

This standard controls the portfolio-facing documentation structure, lab-construction requirements, evidence presentation, screenshot workflow, and publication quality for both approved courses:

- Linux Security
- SOC Analyst — Detection, Adversary Tactics & Incident Handling

It does not decide canonical lab numbering, completion state, execution-system placement, VLAN membership, IP addressing, or operational infrastructure readiness.

Do not change, reinterpret, optimize, add, remove, rename, or reorder the required portfolio README sections unless the user explicitly authorizes a documentation-format change. Only lab-specific technical content may change.

## Lab Construction Baseline

Every newly generated lab must preserve the established instructional depth and portfolio rigor.

- Do not abbreviate a lab merely because the topic is advanced.
- Provide a detailed, sequential walkthrough with explanations before actions.
- Explain what each command does and explain every flag or significant argument used.
- Introduce a major tool before expecting independent use.
- Include verification checkpoints at meaningful technical milestones.
- Request screenshots immediately after the verified result they are intended to prove.
- Preserve evidence only when it materially supports the lab objective, a control, a finding, remediation, or validation.
- Later labs may require more independent reasoning, but they must not reduce documentation depth, verification rigor, screenshot expectations, or evidence quality.

## Required Portfolio README Section Order

Use exactly these eight H2 sections and no others:

1. Project Summary
2. Environment
3. Investigation Scenario
4. Investigation Workflow
5. Key Findings
6. Selected Commands
7. Skills Demonstrated
8. Security Relevance

### Project Summary

Write two substantive paragraphs describing the lab-specific investigation, primary security objective, controlled scenario, validation performed, and final security outcome.

### Environment

Use only `System` and `Role`.

| System | Role |
| --- | --- |
| Lab-specific system type | Lab-specific role in the investigation |

Do not publish hostname, username, IP address, password, token, secret, or other unnecessary identifier in this table.

### Investigation Scenario

Use exactly five practical questions aligned to the canonical lab objective.

### Investigation Workflow

Use a numbered chronology of the work actually performed. Preserve the order of investigation, validation, remediation, positive testing, negative testing, evidence collection, and integrity verification when those activities apply.

Never present planned, skipped, failed, or unverified work as completed.

### Key Findings

Use concise bullets containing only findings supported by retained evidence.

### Selected Commands

Use one concise paragraph linking to [`commands.md`](commands.md) and describing the command categories materially used in the lab.

### Skills Demonstrated

Use one concise prose paragraph describing only skills actually demonstrated and verified.

### Security Relevance

Use one substantive prose paragraph connecting the verified work to practical security operations, administration, detection, incident response, identity, networking, risk reduction, or the lab's canonical objective.

## Tool Education Rule

Every tool must be introduced and taught before the learner is expected to use it independently.

The first substantive use of a tool must explain:

- what the tool is;
- its security purpose;
- how it works at the level needed for the lab;
- where it fits within the lab architecture;
- important terminology;
- basic operation;
- how to interpret its output; and
- the commands, flags, filters, query syntax, or interface elements required for the exercise.

Major platforms may receive dedicated introductory labs. Subsequent labs should increasingly use the tool to accomplish security objectives instead of repeatedly reteaching basic operation. A tool may be a learning objective when first introduced; later labs should measure the security capability demonstrated with it.

Recommended progression:

Tool Primer → Guided Orientation → Guided Practice → Operational Verification → Analyst Use Case → Investigation → Evidence → Result Interpretation → Independent Analyst Task → Reuse in Later Labs.

## Screenshot Requirements

Every newly generated lab requires at least **5 required GitHub screenshots**.

Use the established filename pattern:

`NN-lab-XX-description.png`

`NN` is the screenshot sequence and `XX` is the canonical lab number.

Request only a required screenshot immediately after the result has been verified.

Use exactly this prompt structure:

Required GitHub Screenshot  
Filename:  
`exact filename`

Visual example — frame your screenshot like this:

```text
terminal/interface mockup
```

Match this view:  
State exactly what verified result must be visible.

Redact:  
State exactly what sensitive data, if any, must be hidden.

Screenshot source folders remain device-specific:

| Platform | Screenshot source |
| --- | --- |
| Windows | `C:\Pictures\lab-XX-pics` |
| Linux | `~/Pictures/lab-XX-pics` |

The active course and lab must be explicitly identified before evidence publication so identically numbered Linux and SOC labs cannot be confused.

Updater scripts must validate and copy the exact required screenshot filenames. They must fail closed if a required screenshot is missing, empty, incorrectly named, ambiguous, or unavailable. Do not rename, substitute, infer, or silently skip required screenshots.

Historical completed labs retain their existing evidence counts and filenames unless the user explicitly authorizes a correction.

## Evidence and Integrity Rules

Evidence-dependent workflows must fail closed when expected evidence is missing, empty, unexpected, ambiguous, or fails integrity validation.

- Verify the checksum manifest exists and is non-empty.
- Verify retained evidence against its checksum manifest before publication.
- Do not imply that unlisted files were verified.
- A checksum verifies retained-file integrity; it does not independently prove that an operational security claim is true.
- Do not weaken account, directory, host, or network security merely to simplify evidence retrieval.
- Do not execute untrusted/discovered scripts, binaries, commands, or service-startup instructions unless controlled execution is an explicit safe lab requirement.
- Do not publish passwords, private keys, tokens, domain secrets, API keys, public/ISP WAN information, full MAC addresses, SNMP secrets, serial numbers, or unnecessary sensitive identifiers.

## commands.md

Every completed lab uses `commands.md`.

Keep it concise and focused on commands, query syntax, filters, and operations that materially demonstrate the investigation. Commands used in the instructional walkthrough must be explained when introduced; `commands.md` is a portfolio reference, not a substitute for instruction.

## Lab Closing

Do not include `Lab Completion Requirements` or `Best Way to Add This Lesson to GitHub`.

Close the instructional lab exactly in this order:

1. `Why These Skills Matter`
2. `These Techniques Apply To`
3. `Key Lessons`
4. `Challenge Exercise`
5. `Knowledge Check`

`Knowledge Check` is final.

`Challenge Exercise` must include:

- Scenario
- Requirements/Tasks
- Answers/Solution

## GitHub Paths

Repository: `TreySecurityLab/cyber-portfolio`

Linux Security uses:

`Module-XX-<Module-Name>/Lab-XX-<Lab-Name>/`

SOC Analyst — Detection, Adversary Tactics & Incident Handling uses:

`SOC-Analyst/Module-XX-<Module-Name>/Lab-XX-<Lab-Name>/`

Preserve unrelated repository content and all completed historical Linux lab artifacts.

The root `## Completed Modules` section lists only fully completed modules and clearly identifies the course when more than one course has completed modules.

## Updater and Publication Baseline

When a lab is explicitly complete, its first updater uses the established name:

`update-lab-XX-lean-portfolio.sh`

Version suffixes are reserved for later revisions.

Equivalent Windows and Linux native workflows may be generated as established by the execution standards. The updater itself must validate the target course, canonical lab number, module path, repository, branch, and evidence source so an identically numbered lab from the other course cannot be published to the wrong path.

Updaters must:

- validate the correct repository;
- require branch `main`;
- require a clean starting worktree;
- create a backup;
- retrieve and validate evidence before repository modification;
- fail closed on evidence problems;
- update only required portfolio files;
- validate exact screenshots and checksum manifests;
- show final Git status and diff checks; and
- never mark a lab complete unless the user explicitly confirmed completion.

## Change Control

This standard is shared and independently locked from both course execution standards.

Curriculum changes belong in the matching authoritative curriculum. Completion-state changes belong in the matching course-progress file. Systems, paths, VLANs, host roles, FQDNs, virtualization placement, firewall behavior, evidence collection locations, and operational prerequisites belong in the matching course execution standard or the dedicated home-lab authoritative source.
