![Identity Forensics Playbook](./images/readme-banner-02.png)
<p align="center" style="margin-top: -20px; margin-bottom: -30px;">
  <img src="./images/banner.png" alt="Identity Forensics Playbook" />
</p>

<p align="center">
  <b>Identity‑aware, defensible Microsoft 365 evidence mapping for litigation and cross‑border investigations.</b>
</p>

<p align="center">
  #quick-demoQuick Demo</a> •
  #what-this-repo-isWhat this repo is</a> •
  #methodMethod</a> •
  <a href="#examples/a> •
  <a href="#scripts--ripts & Queries</a> •
  <a href="#lesDeliverables</a> •
  <a href="#crossotesCross‑Border Notes</a>
</p>

---

## What this repo is
**Identity Forensics** turns Microsoft 365 tenant signals (Entra ID sign‑ins, Teams memberships, SharePoint/OneDrive share‑links, mailbox rules, OAuth grants) into a **legally traceable scope** and a **counsel‑ready evidence bundle**.  
The focus is practical: **avoid re‑collections**, **close Teams/SharePoint gaps**, and **ship time‑bounded exports with hashes and manifests**—using built‑in Microsoft tooling.

**Who it’s for**
- Litigation teams, LSPs, and investigations using Microsoft 365.
- Cross‑border operations (e.g., Canada ↔ China/EU subsidiaries) needing **in‑region** collection patterns and **least‑intrusive** scope.

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
#   EX01: Teams Gap (guest/historic identity reveals missing items)
code examples/ex01-teams-gap/README.md

## Roadmap

- [ ] Add synthetic sample datasets for identity signals
- [ ] Build EX03 – OAuth Exfiltration
- [ ] Build EX04 – Dev Tenant Bypass
- [ ] Build EX05 – Legacy Auth Evidence
- [ ] Add Purview KQL queries
- [ ] Add PowerShell Graph extraction scripts
- [ ] Publish 3-part Identity Forensics series on LinkedIn
