# Rules of Engagement

## Purpose

This document defines the legal, ethical, and safety boundaries for all work performed in the AI Cyber Defense Lab repository.

The goal of this lab is to build real cybersecurity investigation and defense skills while staying within authorized, legal, and portfolio-safe environments.

## Core Principle

All security testing must be authorized.

If I do not own the system, control the environment, or have clear written permission to test it, I do not test it.

## Allowed Environments

Security testing, scanning, exploitation practice, and tool usage are allowed only in the following environments:

- My own local machines
- My own virtual machines
- Intentionally vulnerable virtual machines
- Capture-the-Flag labs
- Training platforms
- Sandboxed lab networks
- Authorized classroom or employer-provided labs
- Systems where I have clear written permission to test

Examples of acceptable platforms include:

- TryHackMe
- Hack The Box
- CyberDefenders
- Blue Team Labs
- LetsDefend
- PortSwigger Web Security Academy
- OWASP Juice Shop
- DVWA
- Metasploitable
- Local Kali Linux labs
- Local Windows or Linux victim virtual machines
- Local or authorized AI security labs

## Prohibited Activity

The following activities are not allowed in this lab:

- Attacking real systems without authorization
- Scanning public IP ranges without permission
- Attempting to access accounts I do not own
- Stealing, collecting, or using real credentials
- Deploying malware against real systems
- Evading detection in real environments
- Bypassing security controls on systems I do not own
- Hacking back
- Harassing, doxxing, or targeting individuals
- Testing against employers, vendors, schools, healthcare organizations, or public services without explicit written authorization
- Using this lab to enable crime, abuse, fraud, or unauthorized access

## Offensive Tool Usage

Offensive security tools may be studied and used only for legal defensive education.

Tools such as Kali Linux, Nmap, Burp Suite, Metasploit, Wireshark, and similar utilities may be used only inside approved lab environments or authorized platforms.

The purpose of using these tools is to understand:

- What attackers do
- Why attacks work
- What evidence attacks leave behind
- How defenders detect attacks
- How organizations can reduce risk

## Evidence Handling

Any evidence collected during labs should come from simulated, local, or authorized environments.

Real personal data, protected health information, credentials, private company data, or sensitive third-party information should not be uploaded to this repository.

Screenshots, logs, and artifacts must be reviewed before publishing to make sure they do not expose sensitive information.

## Healthcare Data Boundary

Because my background includes healthcare operations and regulated workflows, I will be especially careful with healthcare-related examples.

This repository must not include:

- Real patient names
- Medical record numbers
- Dates of birth
- Social Security numbers
- Insurance IDs
- Protected health information
- Employer or vendor confidential data
- Internal work documents
- Screenshots from production systems

Healthcare-related projects must use fictional, synthetic, anonymized, or publicly available training data.

## AI Security Boundary

AI security labs must be performed only against:

- My own local models
- Toy applications
- Intentionally vulnerable AI labs
- Authorized test environments
- Simulated data

This repository will not include prompts, workflows, or tooling designed to steal secrets, bypass real access controls, or attack production AI systems.

## AI Use Standard

AI may be used as a tutor, assistant, editor, and analysis support tool.

However, AI output must be verified before being treated as true.

The standard is:

**AI-assisted, human-verified.**

AI can help with:

- Explaining concepts
- Summarizing logs
- Drafting checklists
- Suggesting detection ideas
- Creating study questions
- Reviewing documentation
- Helping structure reports

AI cannot replace:

- Legal authorization
- Human judgment
- Evidence review
- Source verification
- Personal understanding
- Final responsibility for conclusions

## Documentation Standard

Each lab should clearly identify:

- Objective
- Environment
- Rules of Engagement
- Scenario
- Steps Performed
- Findings
- Evidence
- MITRE ATT&CK Mapping, when applicable
- AI Layer / AI Security Relevance, when applicable
- Defensive Takeaways
- Business Impact
- Lessons Learned
- Next Steps

## Public Repository Safety

Before publishing anything to GitHub, I will check for:

- Passwords
- API keys
- Tokens
- Private keys
- Private IP details that should not be shared
- Personal information
- Employer information
- Patient information
- Sensitive screenshots
- Downloaded malware samples
- Anything that could enable misuse

## Professional Standard

This lab exists to build trustworthy defensive capability.

The standard is simple:

If I would not be comfortable explaining the activity to a hiring manager, instructor, or legal authority, it does not belong in this repository.

## Summary

This project is about becoming a capable cyber investigator and defender.

The work must be:

- Legal
- Ethical
- Authorized
- Documented
- Defensive in purpose
- Safe to publish
- Useful as hiring proof