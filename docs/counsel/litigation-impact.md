# Litigation Impact of Identity Forensics (For Counsel)

**Audience:** Litigation counsel, eDiscovery PMs, review managers  
**Purpose:** Explain how Identity Forensics (IF) reduces re‑collections and motion practice risk by aligning discovery scope with how people actually work in Microsoft 365 (work/historic UPNs, guest accounts, and—when signals justify—personal accounts).

---

## 1) The litigation problem Identity Forensics solves

- **Default M365 collections are identity‑blind.**  
  Traditional, mailbox‑centric pulls assume the custodian has *one* account and *one* repository (their current mailbox/OneDrive). In reality, people operate under **multiple identities**: current UPN, **historic** UPNs (name/domain changes), **guest** accounts in partner tenants, and sometimes a **personal Microsoft Account** (MSA) on mobile.

- **Resulting gaps create litigation risk.**  
  Missing Teams messages, absent OneDrive/SharePoint files, and inconsistent audit trails trigger **re‑collections**, **schedule slips**, and **search‑adequacy challenges** (with the potential for sanctions or adverse inference if diligence is questioned).

**Identity Forensics** fixes this by mapping the custodian’s identity footprint and expanding scope **only where signals justify it** (teams membership, share links, mailbox rules, OAuth grants), yielding a **complete, proportional, and defensible** evidence set.

---

## 2) How IF supports your discovery obligations

### A. Reasonable search & search adequacy  
IF documents exactly *why* each location is in scope (identity signals → location), demonstrating a **reasonable, good‑faith search** if challenged. The method prevents the appearance of cherry‑picking tenant‑convenient sources while remaining **targeted** and **time‑bounded**.

### B. Proportionality & least‑intrusive means  
Scope expansion is tied to **observable activity** (e.g., guest posts in a partner Team; files shared to specific external recipients). Personal accounts are considered **only** when there are corporate‑use indicators (e.g., server‑side forwarding). This balances burden with the need for completeness.

### C. Chain of custody & defensibility  
Identity‑aware exports are hashed, time‑bounded, and accompanied by a **manifest** (sources, operator, tool versions, hashes). A one‑page **identity map** makes the collection rationale explainable to the court.

---

## 3) Where IF changes outcomes in a case

1. **Early Case Assessment (ECA).**  
   Surface identity‑driven risks before you promise scope or deadlines. IF prevents “surprise” guest channels and external share paths from emerging late in the schedule.

2. **Collection planning.**  
   Replace vague “tenant mailbox + OneDrive” with **identity‑expanded scope**: primary + historic UPN mailboxes, Teams (member + guest), SharePoint sites tied to share links, and—when warranted—evidence of forwarding/OAuth paths.

3. **Pre‑production validation.**  
   Confirm there are no unexplained gaps. The **added‑hits summary** (delta vs. default collection) shows exactly what identity expansion found and why it matters.

4. **Motion practice & meet‑and‑confer.**  
   A documented identity map and manifest show diligence, proportionality, and a defensible methodology—often enough to avoid motions or resolve disputes quickly.

---

## 4) Practical deliverables you can expect (counsel‑ready)

- **Identity Map (1 page, visual).**  
  Shows Work / Historic / Guest /(if justified) Personal identities and the resources they touched (Teams/SharePoint/Exchange).

- **Added‑Hits Summary (CSV).**  
  The incremental Teams posts, linked files, or mailboxes discovered **only** after identity expansion.

- **Evidence Bundle + Manifest.**  
  Time‑bounded CSV/JSON exports with SHA‑256 hashes, operator, tool versions, and source systems.

- **Two‑Page Brief (plain English).**  
  Why default collection missed items, how IF fixed it, and what was added to scope (forwardable to partners/clients).

---

## 5) Counsel checklists that materially change scope

- **UPNs:** Current and **historic** addresses?  
- **Teams:** Any **guest** participation in external/partner channels?  
- **Sharing:** Files shared externally? **Which link types** (specific‑people, people‑with‑link)?  
- **Rules:** Any **server‑side forwarding/redirect/BCC** rules?  
- **Apps:** Any **OAuth‑connected** third‑party apps during the period?  
- **Devices:** Any **personal** or unmanaged devices for work content?  
- **Window & holds:** Confirm UTC range, legal holds, retention policies.

> Use the intake tools in `/method/` to formalize these answers.

---

