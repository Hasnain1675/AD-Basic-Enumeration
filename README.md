# Active Directory Enumeration Lab

## Overview
This repository documents my hands-on experience with
TryHackMe's AD Basic Enumeration room — part of the
Jr. Penetration Tester learning path.

## Lab Environment
- Target Subnet: 10.211.11.0/24
- Domain: tryhackme.loc
- Domain Controller: 10.211.11.10
- Workstation: 10.211.11.20

## What I Learned
- Network scanning and live host discovery
- Identifying Domain Controllers via port scanning
- Enumerating users through LDAP, SMB, and RPC
- Validating accounts using Kerberos-based tools
- Executing controlled password spraying attacks

## Tools Used
| Tool | Purpose |
|------|---------|
| fping | Live host discovery |
| nmap | Port scanning |
| enum4linux-ng | Full AD enumeration |
| rpcclient | RPC null session |
| ldapsearch | LDAP enumeration |
| kerbrute | User validation |

## Phases Covered
1. Host Discovery
2. Port Scanning
3. User Enumeration
4. Password Spraying

## Disclaimer
All techniques were practiced in an authorized lab
environment provided by TryHackMe. Never use these
techniques on systems without explicit written permission.

## Platform
TryHackMe — Jr Penetration Tester Path
Room: AD Basic Enumeration
