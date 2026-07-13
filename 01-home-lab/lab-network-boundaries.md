# Lab Network Boundaries

## Purpose

This document defines the network boundaries for the AI Cyber Defense Lab.

The goal is to prevent accidental testing against unauthorized systems and to keep vulnerable machines isolated.

## Core Boundary Rule

If a system is not owned by me, intentionally vulnerable, part of a training platform, or clearly authorized, it is out of scope.

## Allowed Network Activity

Allowed network activity includes:

- Communication between my own lab VMs
- Scanning my own local lab targets
- Capturing traffic from my own lab environment
- Accessing authorized training platforms
- Downloading software from official sources
- Updating lab VMs from official repositories

## Prohibited Network Activity

Prohibited network activity includes:

- Scanning random public IP addresses
- Scanning employer systems
- Scanning healthcare systems
- Scanning vendor systems
- Testing websites without written permission
- Attempting to log into accounts I do not own
- Running tools against public targets without authorization
- Exposing vulnerable VMs directly to the internet

## Network Modes

### NAT

NAT usually allows a VM to reach the internet through the host machine.

Possible uses:

- Software updates
- Downloading tools from official sources
- Accessing training platforms

Risk:

- The VM can reach outside systems, so tools must be used carefully.

### Bridged Adapter

Bridged mode places the VM directly on the same network as the host.

Possible uses:

- Advanced networking practice later

Risk:

- The VM may be exposed to the local network.
- Vulnerable machines should generally not use bridged mode.

Default beginner rule:

Avoid bridged mode for vulnerable targets unless there is a specific reason and the risk is understood.

### Host-Only Adapter

Host-only mode allows communication between the host and VMs but does not normally expose the VM to the wider internet.

Possible uses:

- Safe local VM-to-VM labs
- Isolated testing
- Scanning lab targets

Preferred use:

Host-only is preferred for vulnerable targets when possible.

### Internal Network

Internal network mode allows VMs to communicate with each other but not with the host or internet unless configured.

Possible uses:

- More isolated lab environments
- Controlled attacker/target setups

Preferred use:

Internal network is useful when the lab should be separated from both the internet and the host network.

## Initial Safety Model

The initial lab should follow this model:

```text
Kali Linux VM
    ↓
Isolated lab network
    ↓
Vulnerable target VM