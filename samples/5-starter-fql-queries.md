# 5 Free Falcon FQL Queries (sample)

A free sample from **[GhostIntel Press](https://ghosintel.es)** by GhostIntel Press. Paste them into your Falcon console and adapt. Each line is real, executable FQL.

> These 5 cover 5 different ATT&CK tactics. Real, executable, false-positive-aware — a taste of the FQL inside the CCFA bundle.

## 1. Office spawning shell or scripting interpreter
**MITRE:** `T1566.001` &nbsp;·&nbsp; **Tactic:** Initial Access &nbsp;·&nbsp; **Severity:** Critical &nbsp;·&nbsp; **FP level:** very_low

```
event_simpleName=ProcessRollup2 | filter ParentImageFileName IN("WINWORD.EXE","EXCEL.EXE","POWERPNT.EXE","OUTLOOK.EXE") AND ImageFileName IN("cmd.exe","powershell.exe","wscript.exe","cscript.exe","mshta.exe","rundll32.exe") | stats count() by aid, UserName, ParentImageFileName, ImageFileName, CommandLine
```
> Investigate every hit. Legitimate legacy macros should be migrated.

## 2. PowerShell encoded command
**MITRE:** `T1059.001` &nbsp;·&nbsp; **Tactic:** Execution &nbsp;·&nbsp; **Severity:** High &nbsp;·&nbsp; **FP level:** low

```
event_simpleName=ProcessRollup2 | filter ImageFileName="powershell.exe" AND (CommandLine~"-enc " OR CommandLine~"-EncodedCommand" OR CommandLine~"FromBase64String") | stats count() by aid, UserName, CommandLine
```
> Tune by trusted parents.

## 3. Registry Run key write
**MITRE:** `T1547.001` &nbsp;·&nbsp; **Tactic:** Persistence &nbsp;·&nbsp; **Severity:** High &nbsp;·&nbsp; **FP level:** medium

```
event_simpleName=AsepValueUpdate | filter RegObjectName~"CurrentVersion\\\\Run" AND ProcessImageFileName!~"explorer.exe" AND ProcessImageFileName!~"msiexec.exe" | stats count() by aid, UserName, RegObjectName, RegStringValue, ProcessImageFileName
```
> Whitelist signed installers.

## 4. UAC bypass via fodhelper
**MITRE:** `T1548.002` &nbsp;·&nbsp; **Tactic:** Privilege Escalation &nbsp;·&nbsp; **Severity:** Critical &nbsp;·&nbsp; **FP level:** none

```
event_simpleName=ProcessRollup2 | filter ParentImageFileName="fodhelper.exe" AND ImageFileName!~"fodhelper.exe" | stats count() by aid, UserName, ImageFileName, CommandLine
```
> Always investigate. Textbook UAC bypass.

## 5. Event log cleared
**MITRE:** `T1070.001` &nbsp;·&nbsp; **Tactic:** Defense Evasion &nbsp;·&nbsp; **Severity:** Critical &nbsp;·&nbsp; **FP level:** very_low

```
event_simpleName=ProcessRollup2 | filter ImageFileName IN("wevtutil.exe","powershell.exe","cmd.exe") AND (CommandLine~"cl Security" OR CommandLine~"Clear-EventLog" OR CommandLine~"wevtutil cl") | stats count() by aid, UserName, CommandLine
```
> Cross-ref ITSM change calendar.

---

## Preparing the CCFA / CCFR exam?
The **CCFA + CCFR Master Bundle** packs **30 bonus FQL** with 600 explained questions, 2 mock exams and a 77-page masterclass PDF (EN/ES). **€49** · launch **€24,50** with `LAUNCH50` → https://ghosintel.es/l/falcon-ccfa-ccfr-exam-prep

*Not affiliated with CrowdStrike. Test every detection in your environment before relying on it.*
