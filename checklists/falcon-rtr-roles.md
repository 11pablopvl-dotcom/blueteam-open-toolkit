# Falcon Real Time Response (RTR) — Roles Cheat Sheet

RTR lets analysts run commands on a remote host live. **Which role can do what** is a classic CCFA point *and* a real least-privilege decision. Three roles, escalating capability:

| Role | Can do | Cannot do |
|---|---|---|
| **RTR Read-Only Analyst** | Read-only, non-invasive commands: `ls`, `ps`, `netstat`, `reg query`, `ipconfig`, `filehash`, `env`, `cat` | Change anything on the host, put/get files, run scripts |
| **RTR Active Responder** | Everything Read-Only **+** `put` / `get` files, run custom scripts, `rm`, `kill`, `mkdir`, `mv`, restore quarantine | Manage which scripts/files exist in the RTR library, change RTR settings |
| **RTR Administrator** | Everything Active Responder **+** manage the custom **scripts & files library**, manage RTR policy/settings | — (top of the RTR ladder) |

## How to remember it
> **Read-Only = Reads. Active Responder = Acts. Administrator = Administers (the library + settings).**

## Least-privilege guidance
- Tier-1 triage → **Read-Only**. Most investigation lives here.
- Containment/eradication actions → **Active Responder**, granted to senior analysts/IR.
- **Administrator** → very few people; managing the scripts library is powerful (a malicious or sloppy script runs everywhere).
- All RTR actions are **audited** — review the RTR audit logs as part of your detection program.

> Going for the CCFR exam? The **CCFA + CCFR Master Bundle** covers detection triage, RTR and response end-to-end → [GhostIntel Press](https://ghosintel.es/l/falcon-ccfa-ccfr-exam-prep)

*Roles and command availability are configurable and evolve — confirm exact command-to-role mapping in your tenant and the official CrowdStrike docs. Not affiliated with CrowdStrike.*
