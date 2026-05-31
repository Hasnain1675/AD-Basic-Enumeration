# Phase 2: Port Scanning
 

## Objective
Identify the Domain Controller and discover running services.

## Key Active Directory Ports
| Port | Protocol | Purpose |
|------|----------|---------|
| 88   | Kerberos  | Authentication |
| 135  | MS-RPC    | Remote procedure calls |
| 139  | SMB/NetBIOS | Legacy file sharing |
| 389  | LDAP      | Directory queries |
| 445  | SMB       | Modern file sharing |
| 464  | Kerberos  | Password service |

## Targeted Port Scan
```bash
nmap -p 88,135,139,389,445 -sV -sC -iL hosts.txt
```

### Flags
- -sV : Detect service versions
- -sC : Run default scripts
- -iL : Read targets from file

## Full Port Scan
```bash
nmap -sS -p- -T3 -iL hosts.txt -oN full_port_scan.txt
```

### Flags
- -sS : Stealth SYN scan
- -p- : Scan all 65535 ports
- -T3 : Normal timing
- -oN : Save output to file
