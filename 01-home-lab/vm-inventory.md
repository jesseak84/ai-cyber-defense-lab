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
| Internal Storage Used | 842 GB used |
| Approximate Internal Free Space | 112 GB |

## Lab Capacity Assessment

This machine can support a lean-to-medium cybersecurity lab.

Recommended beginner operating model:

- Run Kali Linux plus one target VM at a time.
- Avoid running multiple heavy VMs at once.
- Keep vulnerable target systems isolated.
- Delay heavier Windows test VM work unless storage and performance allow it.
- Store large VM files on an external drive instead of the internal laptop drive.

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