# MITRE ATT&CK — Enterprise Tactics Quick Map

The 14 Enterprise tactics, in attack order. Use this as a mental model when triaging a detection: *where in the kill chain am I, and what comes next?*

| # | Tactic | ID | What the adversary is trying to do | Watch for |
|---|---|---|---|---|
| 1 | Reconnaissance | TA0043 | Gather info to plan the operation | Scanning, OSINT, phishing for info |
| 2 | Resource Development | TA0042 | Build/buy/steal capabilities | Domain reg, malware staging, fake accounts |
| 3 | Initial Access | TA0001 | Get a foothold | Phishing, valid accounts, public-facing exploit |
| 4 | Execution | TA0002 | Run attacker code | PowerShell, WMI, scheduled tasks, signed binaries |
| 5 | Persistence | TA0003 | Keep access across reboots/creds | Run keys, services, scheduled tasks, WMI subs |
| 6 | Privilege Escalation | TA0004 | Get higher permissions | Token theft, UAC bypass, exploit, IFEO |
| 7 | Defense Evasion | TA0005 | Avoid being detected | Obfuscation, disabling tools, ETW patching, LOLBins |
| 8 | Credential Access | TA0006 | Steal account names/passwords | LSASS dump, Kerberoasting, cred stores |
| 9 | Discovery | TA0007 | Learn the environment | `whoami`, AD enumeration, network/host recon |
| 10 | Lateral Movement | TA0008 | Move through the network | RDP, PsExec, WMI, pass-the-hash |
| 11 | Collection | TA0009 | Gather target data | Screen capture, keylogging, archive staging |
| 12 | Command & Control | TA0011 | Talk to compromised hosts | Beaconing, DNS/HTTPS C2, domain fronting |
| 13 | Exfiltration | TA0010 | Steal the data out | C2 channel transfer, cloud upload, DNS tunneling |
| 14 | Impact | TA0040 | Disrupt/destroy/extort | Ransomware, wiping, defacement, account lockout |

## How to use it in detection engineering
1. **Map every detection to a tactic + technique** — coverage gaps become obvious.
2. **Don't over-invest in one tactic.** Most teams over-cover Execution and under-cover Defense Evasion + Credential Access.
3. **Pair with [DeTT&CT](https://github.com/rabobank-cdc/DeTTECT)** to score your data-source visibility per tactic.

> Preparing CCFA / CCFR? The **Master Bundle** maps detection investigation to these tactics with 600 explained questions → [GhostIntel Press](https://ghosintel.es/l/falcon-ccfa-ccfr-exam-prep)

*Source: [attack.mitre.org](https://attack.mitre.org/). Public framework — verify technique IDs against the live matrix.*
