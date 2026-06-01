# CCFA Study Roadmap (free)

A realistic plan to pass the **CrowdStrike Certified Falcon Administrator (CCFA)** — built from passing it, not from a generic Q&A dump.

## The exam, briefly
- **~60 questions · ~90 minutes**, multiple choice.
- Tests **administering** Falcon: platform architecture, sensor lifecycle, host management, policies, detections & response, and supporting modules.
- **Verify the current format, cost and objective weights on the official CrowdStrike certification page** before you book — they change. Don't trust any third party (including us) for the live numbers.

## What actually trips people up (study these hard)
These are concept pairs people fail on. Master the *difference*, not the definition:
- **CID vs AID** — CID = customer/tenant scope; AID = one sensor instance. (The names feel backwards — that's the trap.)
- **IOA vs IOC** — behaviour-based vs artifact-based.
- **Prevention vs Detection policy** — what blocks vs what only alerts.
- **RFM (Reduced Functionality Mode)** — triggered by kernel/compatibility issues, *not* by containment. See [`falcon-rtr-roles.md`](falcon-rtr-roles.md) for the related RTR roles.
- **Host states** — Online vs Reduced Functionality vs **inactive** (Falcon flags a host inactive after it stops checking in — confirm the current threshold on the official docs; it's commonly cited as ~7 days, and sensors are auto-removed after a longer window).
- **Detection severity is independent of whether the activity was blocked.**
- **Network Containment** keeps the Falcon cloud channel open while isolating the host from everything else.

## A 3-week plan
**Week 1 — Foundations.** Platform architecture (sensor → cloud → Threat Graph), sensor deployment & update policies, host groups. Build the mental model first.
**Week 2 — Operations.** Prevention/detection policies, the detections workflow, RTR, exclusions, dashboards & reports.
**Week 3 — Drill & gaps.** Timed practice. Track *which domain* you miss, not just your score, and go back to that area. Do a full timed mock 48h before, then rest.

## Free resources to use
- Official CrowdStrike certification page (book + verify objectives)
- [CrowdStrike Community](https://community.crowdstrike.com/) and [r/crowdstrike](https://www.reddit.com/r/crowdstrike/)
- [MITRE ATT&CK tactics map](mitre-attack-tactics.md) (this repo)

## When free isn't enough
The hardest part is **realistic, explained practice questions** — that's the gap most Spanish-speaking candidates hit.

> **CCFA + CCFR Master Bundle** → 600 questions (330 EN + 270 ES · offline, no login), 2 timed mock exams, 77-page Spring-2026 PDF, editable JSON bank + 2-week recovery plan. Covers 100% CCFA + ~70% CCFR. Pass without the ~€2,000 official course.
> 👉 **€49** · launch **€24,50** with code `LAUNCH50` → https://ghosintel.gumroad.com/l/falcon-ccfa-ccfr-exam-prep

*Not affiliated with CrowdStrike. Based on publicly documented exam objectives.*
