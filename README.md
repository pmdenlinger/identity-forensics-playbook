![Identity Forensics Playbook](./images/readme-banner-02.png)

<p align="center" style="margin-top: -10px; margin-bottom: -20px;">
  ./images/readme-banner-02.png
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Maintained-Yes <img src="https://img.shields.io/badge/Status-In%20Development-yellow" alt="s://img.shields.io/badge/Focus-M365%20Identity%20Forensics-blue" alt="Focusmg.shields.io/badge/Scope-Identity%20Aware-8A2BE2" alt="In Development Status" />

<p align="center">
  <b>Identity‑aware, defensible Microsoft 365 evidence mapping for litigation and cross‑border investigations.</b>
</p>

<p align="center">
  #quick-demoQuick Demo</a> •
  #what-this-repo-isWhat this repo is</a> •
  #methodMethod</a> •
  #examplesExamples</a> •
  #scripts--queriesScripts & Queries</a> •
  #deliverablesDeliverables</a> •
  #cross-border-notesCross‑Border Notes</a>
</p>

---

### What this is (and isn’t)

This workbook focuses on identity signals and evidence locations in Microsoft 365:
- Signals: Entra ID sign-ins, Teams memberships, SharePoint/OneDrive share-links, mailbox rules, OAuth grants.
- Locations: Exchange, Teams (member/guest channels), SharePoint/OneDrive drives and sites.


**Who it’s for**

- Litigation teams, LSPs, and investigations using Microsoft 365.
- Cross‑border operations (e.g., Canada ↔ China/EU subsidiaries) needing **in‑region** collection patterns and **least‑intrusive** scope.

### Scope Decision Rule (Signals → Location → Export)
For each candidate location:
1) Signal present? (identity, membership, link, rule, OAuth) 
2) Within window? (UTC start/end) 
3) Least-intrusive? (add only what the signal supports) 
4) Documented? (record signal → reason → export in manifest)

### EDRM Left‑Side Leak Controls
Common leak points (technical):
- Identification: guest identities and historic UPNs not mapped to locations
- Preservation: holds not applied to specific Teams/SPO paths
- Collection: mailbox-only pulls missing Teams/SharePoint content

Control: enumerate identities → map to locations → apply holds/exports → record in manifest (hashes, operator, timestamp).

### Human-in-the-Loop (Quality Control)
A named operator validates:
- Identity map completeness vs. matter custodian list
- Signals → locations linkage (traceability)
- Time-window correctness
- Export integrity (hashes) and manifest accuracy
- Added-hits delta vs. default collection

Purpose: prevent missed sources and re-collections—not to interpret human intent.

---

## Quick Demo

> Run an end‑to‑end, synthetic example to see how identity signals change scope and recover missed items.

```bash
# 1) clone
git clone https://github.com/pmdenlinger/identity-forensics-playbook.git
cd identity-forensics-playbook

# 2) (optional) create a clean Python venv if any helper scripts are added later
# python3 -m venv .venv && source .venv/bin/activate

# 3) open the example and follow its README
#EX01: Teams Gap (guest/historic identity reveals missing items)
code examples/ex01-teams-gap/README.md
```

<p align="center">
  <i>Roadmap: April → August (Pre‑Launch)</i>
</p>

- [ ] Add synthetic sample datasets for identity signals
- [ ] Build EX03 – OAuth Exfiltration
- [ ] Build EX04 – Dev Tenant Bypass
- [ ] Build EX05 – Legacy Auth Evidence
- [ ] Add Purview KQL queries
- [ ] Add PowerShell Graph extraction scripts
- [ ] Publish 3-part Identity Forensics series on LinkedIn

➡️ Jump to: [EX01 TeamsGap
➡️ Jump to: [Method](./method)
