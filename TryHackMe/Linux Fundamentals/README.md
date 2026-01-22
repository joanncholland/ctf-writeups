# Linux Fundamentals

## Overview

Difficulty: Easy  
Skills Tested: Enumeration, SMB exploitation, privilege escalation

## Commands

| Command    |                        Description                         |
| ---------- | :--------------------------------------------------------: |
| echo       |              Output any text that we provide               |
| whoami     |      Find out what user we're currently logged in as!      |
| ls         |        List files and folders in current directory         |
| cd         |                      Change directory                      |
| cat        |            View contents of file (concatenate)             |
| pwd        |                  Print working directory                   |
| find -name |                    Find file with name                     |
| wc         | Word count - can use flags -l (line), -w (word), -c (byte) |
| grep       |              Search file for specific content              |

## Linux Operators

| Operator | Description                                                                                                                                      |
| -------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| &        | Run commands in the background of your terminal                                                                                                  |
| &&       | Combine multiple commands together in one line                                                                                                   |
| >        | This operator is a redirector - meaning that we can take the output from a command (such as using cat to output a file) and direct it elsewhere. |
| >>       | This operator does the same function of the > operator but appends the output rather than replacing (meaning nothing is overwritten).            |

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
