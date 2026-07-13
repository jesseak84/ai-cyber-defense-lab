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

Heavy lab assets will be stored on an external drive instead of the laptop's internal drive.

External lab folder location:

D:\Cyber-Fu-Lab

External lab folder structure:

- Cyber-Fu-Lab/
  - VMs/
    - Kali/
    - Targets/
    - Windows-Test/
    - Snapshots/
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

- Keep large VM files off the internal laptop drive.
- Preserve internal storage for Windows, tools, and normal work.
- Keep lab assets organized.
- Make backups easier.
- Reduce risk of mixing lab evidence with personal or work files.

Important rule:

The GitHub repository stores documentation and sanitized artifacts. The external drive stores heavy VM files, ISOs, captures, screenshots, and working evidence.

Before anything from the external drive is copied into the public GitHub repository, it must be reviewed for sensitive data.