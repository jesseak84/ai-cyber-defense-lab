# VM Inventory

## Purpose

This document tracks virtual machines and lab storage used in the AI Cyber Defense Lab.

The purpose of the inventory is to document what systems exist, what they are used for, where they are stored, and what boundaries apply to them.

## Host Machine

| Item | Details |
|---|---|
| Device | MSI Cyborg 15 A12VF |
| Operating System | Windows 11 |
| CPU | 12th Gen Intel Core i7-12650H |
| RAM | 16 GB |
| GPU | NVIDIA GeForce RTX 4060 Laptop GPU, 8 GB |
| Internal Storage | 954 GB total |
| Approximate Internal Free Space | 336 GB |

## Lab Capacity Assessment

This machine can support a lean-to-medium cybersecurity lab.

Recommended beginner operating model:

- Run Kali Linux plus one target VM at a time.
- Avoid running multiple heavy VMs at once.
- Keep vulnerable target systems isolated.
- Delay heavier Windows test VM work unless storage and performance allow it.
- Store active VMs on the internal C: drive for better performance.
- Store ISOs, backups, evidence, and archived VMs on the external D: drive.

## External Lab Storage Plan

Heavy lab assets will be stored on the external D: drive.

External lab folder location:

D:\Cyber-Fu-Lab

External lab folder structure:

- Cyber-Fu-Lab/
  - VMs-Archive/
  - ISOs/
    - Kali/
    - Windows/
    - Linux/
  - Evidence/
    - screenshots/
    - packet-captures/
    - logs/
  - Backups/

Purpose:

- Store large downloads, ISOs, backups, evidence, and archived VMs outside the laptop's internal drive.
- Keep the internal C: drive available for active VMs that need better performance.
- Keep lab assets organized.
- Make backups easier.
- Reduce risk of mixing lab evidence with personal or work files.

Important rule:

The GitHub repository stores documentation and sanitized artifacts.

The internal C: drive stores active VMs.

The external D: drive stores ISOs, backups, evidence, and archived VMs.

Before anything from the external drive is copied into the public GitHub repository, it must be reviewed for sensitive data.

## Active VM Storage Plan

The internal laptop drive now has enough free space to run active VMs more efficiently.

Active VM location:

C:\Cyber-Fu-Lab\Active-VMs

Active VM folder structure:

- Active-VMs/
  - Kali/
  - Targets/
  - Windows-Test/

Storage/archive location:

D:\Cyber-Fu-Lab

Storage rule:

- Active VMs that need better performance should run from the internal C: drive.
- Large downloads, ISOs, backups, evidence, and archived VMs should be stored on the external D: drive.
- The external D: drive is a spinning hard drive, so it is better for storage than active VM performance.
- Only one main lab target should run alongside Kali at a time unless performance is confirmed stable.

## Virtualization Software Plan

The lab will use VMware Workstation Pro as the primary virtualization platform.

Reason for decision:

- VMware Workstation Pro is the preferred platform for this lab.
- VMware is a strong fit for Kali Linux and local cybersecurity lab work.
- VMware supports snapshots, virtual networking, and stable VM performance.
- Kali provides official VMware images, which should simplify setup.
- VirtualBox remains a fallback only if VMware becomes a real technical blocker.

Current decision:

- Virtualization platform: VMware Workstation Pro
- Status: Selected
- Install status: Installed and opens successfully

Installation note:

- VMware Workstation Pro was installed successfully.
- The application opens on the host machine.
- Next step is to import or create the Kali Linux VM.

Lab operating model:

- Run Kali Linux plus one target VM at a time.
- Store active VMs on the internal C: drive for better performance.
- Store ISOs, backups, evidence, and archived VMs on the external D: drive.

## VM Inventory Table

| VM Name | Role | Operating System | Network Mode | Internet Access | Storage Location | Status | Notes |
|---|---|---|---|---|---|---|---|
| Kali Linux | Analyst / testing VM | Kali Linux | To be determined | Limited / controlled | C:\Cyber-Fu-Lab\Active-VMs\Kali | Planned | Used only in authorized labs |
| Vulnerable Target 1 | Lab target | To be determined | Isolated preferred | No, unless needed | C:\Cyber-Fu-Lab\Active-VMs\Targets | Planned | Example: Metasploitable, DVWA, Juice Shop |
| Windows Test VM | Evidence / victim VM | Windows | To be determined | Limited / controlled | C:\Cyber-Fu-Lab\Active-VMs\Windows-Test | Planned | Used later for Windows logs and DFIR practice |
| Archived VMs | Storage/archive | Various | Not applicable | Not applicable | D:\Cyber-Fu-Lab\VMs-Archive | Planned | Stored on external D: drive |

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

A Windows test VM may be used later for:

- Event Viewer practice
- Login event review
- Suspicious login simulations
- Sysinternals practice
- Basic DFIR artifact review

### Archived VMs

Archived VMs are inactive VM files stored on the external D: drive.

Archived VMs should not be treated as active lab machines until copied back to the active VM location and reviewed.

## Snapshot Plan

Snapshots should be taken:

- After a clean install
- Before major configuration changes
- Before intentionally vulnerable lab activity
- Before risky experiments
- After a known-good configuration

Snapshot naming format:

- YYYY-MM-DD_clean-install
- YYYY-MM-DD_before-lab-name
- YYYY-MM-DD_after-config-change

Snapshot warning:

- Snapshots consume disk space.
- Too many snapshots can create performance and storage problems.
- Only keep snapshots that have a clear purpose.

## Sensitive Data Rule

No VM should contain:

- Real patient data
- Employer data
- Real credentials
- Personal financial records
- Private family information
- Production system screenshots
- Work documents

Labs should use fake, synthetic, public, or training-platform data only.

## Maintenance Notes

Track updates, installs, and changes here.

| Date | VM / Component | Change Made | Reason | Notes |
|---|---|---|---|---|
| 2026-07-13 | Host machine | Documented host specs | Establish lab capacity | MSI Cyborg 15 A12VF |
| 2026-07-13 | Storage plan | Added C: active VM and D: archive plan | Improve VM performance | External D: drive is HDD |
| 2026-07-13 | VMware Workstation Pro | Installed and opened successfully | Primary virtualization platform | Ready for Kali import |

## Current Status

The host machine has been documented.

The storage plan has been documented.

VMware Workstation Pro is installed and opens successfully.

Next steps:

- Download the official Kali Linux VMware image.
- Store downloaded Kali archive under D:\Cyber-Fu-Lab\ISOs\Kali.
- Extract the active Kali VM under C:\Cyber-Fu-Lab\Active-VMs\Kali.
- Open the Kali .vmx file in VMware.
- Confirm Kali VM settings before first boot.