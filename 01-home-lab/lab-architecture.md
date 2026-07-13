# Home Lab Architecture

## Objective

The objective of this lab is to design and document a safe local cybersecurity training environment for the AI Cyber Defense Lab project.

This lab will support legal practice in:

- Networking fundamentals
- Linux and Kali orientation
- Reconnaissance and enumeration against owned targets
- Web security labs
- Phishing and incident response simulations
- Log review and basic forensics
- AI security demonstrations using fake or local data

## Rules of Engagement

This lab is for authorized training only.

Allowed targets include:

- My own virtual machines
- Intentionally vulnerable virtual machines
- Local lab systems
- Training platforms
- Simulated evidence
- Fake or synthetic data

Not allowed:

- Scanning random public IP addresses
- Testing against real websites without written permission
- Using employer systems or data
- Uploading real credentials, patient information, or sensitive work material
- Running malware outside controlled legal labs
- Attempting unauthorized access

## Lab Purpose

The purpose of the home lab is to create a controlled environment where I can safely observe attacker behavior, collect evidence, and document defensive lessons.

This lab is not meant to prove that I can “hack things.”

It is meant to prove that I can:

- Build a safe test environment
- Understand scope and authorization
- Use cybersecurity tools responsibly
- Observe what evidence activity leaves behind
- Write clear documentation
- Connect technical behavior to defensive action
- Build portfolio artifacts that are safe to publish

## Planned Lab Components

### Host Machine

The host machine is my Windows computer.

The host machine will run virtualization software and store lab notes, screenshots, and project documentation.

### Virtualization Platform

Planned virtualization platform:

- VirtualBox or VMware Workstation Player

Final platform selected:

- To be determined

Selection criteria:

- Works reliably on my Windows machine
- Supports Kali Linux
- Supports isolated lab networking
- Allows snapshots
- Is beginner-friendly enough to maintain

### Analyst / Attacker VM

Planned system:

- Kali Linux

Purpose:

Kali will be used as the analyst and testing machine inside authorized labs.

Kali may be used for:

- Linux practice
- Nmap scanning of lab targets
- Web testing against vulnerable apps
- Packet analysis
- Tool familiarization
- Documentation of attacker behavior from a defender’s perspective

Kali will not be used against unauthorized systems.

### Target / Victim VMs

Planned target systems may include:

- Metasploitable
- OWASP Juice Shop
- DVWA
- Windows evaluation VM
- Linux server VM
- Other intentionally vulnerable machines

Purpose:

Target VMs provide safe systems to observe, test, and document security concepts.

### Network Modes

The lab may use multiple network modes depending on the activity.

Common options:

- NAT
- Host-only
- Internal network

The preferred safety model for vulnerable machines is isolation from the public internet unless internet access is specifically needed for updates or training platform access.

## Basic Network Design

Initial planned design:

```text
Windows Host Machine
│
├── Kali Linux VM
│
├── Vulnerable Target VM
│
└── Optional Windows/Linux Evidence VM