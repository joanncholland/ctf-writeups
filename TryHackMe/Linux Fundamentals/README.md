# Machine Name – Hack The Box

## Overview

Difficulty: Easy  
Skills Tested: Enumeration, SMB exploitation, privilege escalation

## Reconnaissance

- Initial Nmap scan revealed ports 21, 22, 445
- SMB allowed anonymous login

## Exploitation

- Enumerated SMB shares using smbclient
- Discovered vulnerable service version
- Exploited using Metasploit/manual exploit

## Privilege Escalation

- Found misconfigured SUID binary
- Leveraged it to gain root access

## Key Takeaways

- Importance of service enumeration
- Risks of anonymous SMB access
- Proper privilege separation

## Real-World Impact

This vulnerability could allow an attacker to:

- Enumerate internal shares
- Escalate privileges to administrator
- Pivot deeper into the network
