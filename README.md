# CrowdStrike Toolkit 🛡️

> **1144 recursos operativos verificados** para CrowdStrike Falcon: queries CQL, dashboards, workflows SOAR, scripts, reglas IOA, integraciones API y material de referencia.
> Maintained by **[GhostIntel Press](https://ghosintel.gumroad.com)**.

If this saves you time, **drop a ⭐** — it's how more blue teamers find it.

---

## 📊 CrowdStrike Toolkit Resources (Excel)

### `CrowdStrike_Toolkit_Resources.xlsx`

Excel estructurado con **1144 recursos** verificados de 20 fuentes, organizado en columnas:

| Columna | Descripción |
|---------|-------------|
| ID | Identificador único secuencial |
| Nombre del Recurso | Nombre descriptivo del recurso |
| Tipo | Query CQL, Dashboard, Workflow, Script, IOA Rule, API Service, etc. |
| Categoría | Clasificación funcional (Threat Hunting, SOAR, NG-SIEM, etc.) |
| Subcategoría | Área específica (Persistence, Credential Access, Network, etc.) |
| MITRE ATT&CK | Técnica MITRE asociada cuando aplica |
| Plataforma | Windows, Linux, Mac, Multi-platform |
| Descripción | Descripción funcional del recurso |
| Autor/Fuente | Creador o fuente del recurso |
| Módulo Requerido | Módulo CrowdStrike necesario (Insight, NG-SIEM, etc.) |
| Log Source | Fuente de datos requerida |
| Año/Fecha | Fecha de publicación o última actualización |
| URL/Referencia | Enlace directo al recurso original |

### Distribución de Recursos

| Tipo de Recurso | Cantidad |
|----------------|----------|
| Queries CQL (Hunting/Detection) | ~550 |
| Dashboards (YAML templates) | ~200 |
| Workflows SOAR | ~35 |
| Scripts de Despliegue | ~20 |
| Custom IOA Rules | ~25 |
| API Service Collections | ~48 |
| Herramientas y Repos GitHub | ~33 |
| Casos de Uso y Capacidades | ~30 |
| Tutoriales y Referencias CQL | ~100 |
| Alertas, Parsers y Scheduled Searches | ~50 |
| Lookup Files y Recursos Auxiliares | ~10 |
| Detection Content (Third-Party) | ~10 |

### Fuentes Principales (20 verificadas)

1. **CrowdStrike/logscale-community-content** — Repositorio oficial comunitario (~600 items)
2. **ByteRay-Labs/Query-Hub (CQL Hub)** — Biblioteca abierta de queries CQL (159 items)
3. **Cool Query Friday (Reddit)** — Serie semanal de 90+ entregas (~51 items)
4. **a2awais/Threat-Hunting** — Queries CQL de threat hunting avanzado (28 items)
5. **CrowdStrike GitHub Organization** — 200+ repos públicos (~33 tools)
6. **FalconPy SDK** — Service collections de la API (~48 services)
7. **CrowdStrike Tech Hub** — Guías técnicas oficiales
8. **Falcon Fusion SOAR Documentation** — Workflows y playbooks (~35 items)

---

## ⚡ Start here — free interactive CCFA quiz
Preparing the **CrowdStrike CCFA / CCFR** exam? **[Launch the free CCFA Starter Kit →](ccfa-free/)** — answer **12 real exam questions** interactively, see the **6-domain exam map**, and grab **5 must-know FQL queries**. No signup.

Prefer raw detections? **5 paste-and-run FQL queries** → **[samples/5-starter-fql-queries.md](samples/5-starter-fql-queries.md)**

---

## 📑 Contents
- [CrowdStrike Toolkit Resources (Excel)](#-crowdstrike-toolkit-resources-excel)
- [Official CrowdStrike & Falcon](#-official-crowdstrike--falcon)
- [MITRE ATT&CK](#-mitre-attck)
- [Detection rules & Sigma](#-detection-rules--sigma)
- [Hands-on labs](#-hands-on-labs)
- [Newsletters & blogs](#-newsletters--blogs)
- [Open-source blue team tools](#-open-source-blue-team-tools)
- [Cheat sheets & checklists (ours, free)](#-cheat-sheets--checklists-ours-free)
- [Get the full toolkit (paid)](#-get-the-full-toolkit)

---

## 🦅 Official CrowdStrike & Falcon
- [CrowdStrike Blog](https://www.crowdstrike.com/blog/) — official research & detections
- [CrowdStrike Community](https://community.crowdstrike.com/) — Q&A, RTR, FQL discussions
- [r/crowdstrike](https://www.reddit.com/r/crowdstrike/) — the place people actually ask CCFA / Falcon questions
- [CrowdStrike Falcon (login)](https://falcon.crowdstrike.com/) — console & in-product docs
- [CrowdStrike Tech Hub](https://www.crowdstrike.com/tech-hub/) — NG-SIEM guides, CQL tutorials
- [LogScale Community Content](https://github.com/CrowdStrike/logscale-community-content) — official queries, dashboards, parsers
- [CQL Hub](https://cql-hub.com/) — community CQL query library
- [FalconPy SDK](https://www.falconpy.io/) — Python SDK for Falcon APIs

## 🎯 MITRE ATT&CK
- [ATT&CK Matrix for Enterprise](https://attack.mitre.org/)
- [ATT&CK Navigator](https://mitre-attack.github.io/attack-navigator/)
- [DeTT&CT](https://github.com/rabobank-cdc/DeTTECT) — score data-source visibility & detection coverage
- Our quick map → [`checklists/mitre-attack-tactics.md`](checklists/mitre-attack-tactics.md)

## 🧩 Detection rules & Sigma
- [Sigma HQ](https://github.com/SigmaHQ/sigma) — generic detection rules + converters
- [awesome-detection-engineering](https://github.com/infosecB/awesome-detection-engineering)
- [awesome-cybersecurity-blueteam](https://github.com/fabacab/awesome-cybersecurity-blueteam)
- [BlueTeam-Tools](https://github.com/A-poc/BlueTeam-Tools)

## 🧪 Hands-on labs
- [DetectionLab](https://github.com/clong/DetectionLab) — full lab with logging + tooling
- [Atomic Red Team](https://github.com/redcanaryco/atomic-red-team) — emulate ATT&CK techniques to test detections

## 📰 Newsletters & blogs
- [Detection Engineering Weekly](https://www.detectionengineering.net/)
- [tl;dr sec](https://tldrsec.com/)

## 🛠️ Open-source blue team tools
- [Velociraptor](https://github.com/Velocidex/velociraptor) — DFIR & hunting
- [Chainsaw](https://github.com/WithSecureLabs/chainsaw) — fast Windows event-log hunting
- [Hayabusa](https://github.com/Yamato-Security/hayabusa) — Sigma-based Windows event-log analysis

## ✅ Cheat sheets & checklists (ours, free)
Practical, vendor-neutral, **no login required**:
- [CCFA study roadmap](checklists/ccfa-prep-roadmap.md) — exam domains + a realistic study plan
- [MITRE ATT&CK tactics quick map](checklists/mitre-attack-tactics.md)
- [Falcon RTR roles cheat](checklists/falcon-rtr-roles.md)

---

## 🚀 The exam prep that isn't a dump
The free resources above point you to the material. The **paid bundle is the synthesized shortcut to actually pass** — legitimate (no NDA dumps), **bilingual (EN + ES)**, built by Pablo Piedrabuena, a cybersecurity expert and Tier-3 (N3) CrowdStrike analyst at one of Spain's largest telecoms, in the field since 2018.

| | What you get | Price |
|---|---|---|
| 🎁 **CCFA Free Starter Kit** | 12 real questions (interactive) + 6-domain exam map + 5 FQL | **Free** → [launch](ccfa-free/) |
| ⭐ **CCFA + CCFR Master Bundle** | **600 questions** (330 EN + 270 ES · offline HTML, no login) + 2 timed mock exams (60 Q each) + 77-page Spring-2026 masterclass PDF + editable JSON bank + 30 bonus FQL — covers 100% CCFA + ~70% CCFR | **€49** |

👉 **Get the bundle → https://ghosintel.gumroad.com/l/falcon-ccfa-ccfr-exam-prep**
🎁 Launch code `LAUNCH50` → **€24,50** (−50%, first 7 days)

---

## 🤝 Contributing
Found a great free resource? Open a PR. Keep it **vendor-honest** and **practitioner-useful** — no dumps, no NDA-violating exam content.

## 📄 License & disclaimer
Curated links belong to their authors. This list and our checklists: **CC BY 4.0**.
**Not affiliated with CrowdStrike.** Independent material based on publicly documented objectives.

Contact: **support@ghosintel.es** · by [GhostIntel Press](https://ghosintel.gumroad.com)

---

*Última actualización: Junio 2026*
