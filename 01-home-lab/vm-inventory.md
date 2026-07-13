# VM Inventory

## Purpose

This document tracks virtual machines used in the AI Cyber Defense Lab.

The purpose of the inventory is to document what systems exist, what they are used for, and what boundaries apply to them.

## Inventory Table

| VM Name | Role | Operating System | Network Mode | Internet Access | Status | Notes |
|---|---|---|---|---|---|---|
| Kali Linux | Analyst / testing VM | Kali Linux | To be determined | Limited / controlled | Planned | Used only in authorized labs |
| Vulnerable Target 1 | Lab target | To be determined | Isolated preferred | No, unless needed | Planned | Example: Metasploitable, DVWA, Juice Shop |
| Windows Test VM | Evidence / victim VM | Windows | To be determined | Limited / controlled | Planned | Used for Windows logs and DFIR practice |
| Linux Test VM | Evidence / victim VM | Linux | To be determined | Limited / controlled | Planned | Used for Linux logs and auth log practice |

## VM Roles

### Analyst / Testing VM

The analyst VM is the system used to run tools, observe traffic, collect evidence, and practice commands.

Initial planned analyst VM:

- Kali Linux

### Vulnerable Target VM

The vulnerable target VM is intentionally unsafe and must be isolated.

Possible examples:

- Metasploitable
- DVWA
- OWASP Juice Shop
- Intentionally vulnerable CTF boxes

These systems should not be exposed to the public internet.

### Windows Test VM

A Windows test VM may be used for:

- Event Viewer practice
- Login event review
- Suspicious login simulations
- Sysinternals practice
- Basic DFIR artifact review

### Linux Test VM

A Linux test VM may be used for:

- Auth log review
- SSH login practice
- File permission practice
- Process and service observation
- Bash command practice

## Snapshot Plan

Snapshots should be taken:

- After a clean install
- Before major configuration changes
- Before intentionally vulnerable lab activity
- Before risky experiments
- After a known-good configuration

Snapshot naming format:

```text
YYYY-MM-DD_clean-install
YYYY-MM-DD_before-lab-name
YYYY-MM-DD_after-config-change