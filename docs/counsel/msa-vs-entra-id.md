# Microsoft Account (MSA) vs. Entra ID (Work/School) – What Counsel Needs to Know

**Audience:** Litigation counsel, eDiscovery PMs, review managers  
**Purpose:** Explain the difference between a *personal* Microsoft Account (**MSA**; e.g., Outlook.com/Hotmail) and a *work/school* account (**Entra ID**; formerly Azure AD). Show why the distinction matters for collections, legal hold, and search adequacy.

---

## The one‑minute version

- **MSA = Personal identity** (e.g., `name@outlook.com`, consumer Microsoft services).  
- **Entra ID = Work/School identity** assigned by the company (e.g., `name@company.com`, used for Microsoft 365, Teams, SharePoint, Exchange).  
- In cloud matters, the same human may use **both**. Evidence can therefore live under **multiple identities**—not just the corporate mailbox/OneDrive.

> **Bottom line:** If you don’t map *all identities a custodian used*, default M365 collections can miss Teams posts, file shares, or messages created with guest/personal contexts. Identity Forensics expands scope *only where signals justify it*.

---

## Key definitions (plain English)

- **Microsoft Account (MSA):** A *personal* Microsoft login (e.g., `outlook.com`, `hotmail.com`) used for consumer services. Users can sign in to certain enterprise links with MSAs (depending on how the link was shared), even from **unmanaged devices**.

- **Entra ID (Work/School):** The organization’s *enterprise directory* identity (formerly “Azure AD”). It controls access to Microsoft 365: Outlook mailboxes, Teams, SharePoint/OneDrive, and applies corporate policies (holds, DLP, retention).

- **Guest account (B2B):** A **cross‑tenant** identity created when your custodian was invited to another org’s team or site. In activity logs, it can appear like `name_example.com#EXT#@yourtenant.onmicrosoft.com`.

---

## Why this matters in litigation

1. **Evidence fragmentation**  
   - A custodian’s evidence may be **split** across:  
     - their *current* Entra ID UPN,  
     - a *historic* UPN (name/domain change),  
     - one or more **guest** identities,  
     - and occasionally a **personal MSA** used from a phone.

2. **Default collections can miss items**  
   - Teams posts while the custodian was a **guest** in a partner team can be **absent** from a tenant‑only pull.  
   - Files shared as **specific‑people** or **people‑with‑link** may be stored on **SharePoint sites** not linked to the custodian’s OneDrive.  
   - Personal device usage + MSA can complicate **audit visibility**.

3. **Defensibility & proportionality**  
   - Mapping identities and expanding scope where signals show activity demonstrates a **reasonable, diligent** search without over‑collecting.

---

## Quick comparison: MSA vs. Entra ID

| Dimension | MSA (Personal Microsoft Account) | Entra ID (Work/School) |
|---|---|---|
| Ownership | Individual (consumer) | Organization (enterprise directory) |
| Typical addresses | `name@outlook.com`, `name@hotmail.com` | `name@company.com` |
| Governance | Not subject to company retention/holds by default | Subject to organizational holds, retention, DLP |
| Usage in matters | Sometimes used to access links from unmanaged devices or mobile apps | Primary identity for mail, Teams, SharePoint, OneDrive |
| Visibility | Limited to what can be proven via corporate signals (e.g., link access, forwarding rules) | Full visibility under tenant controls, logs, exports |
| Risk | Potential **exfiltration path** or off‑tenant evidence | Normal corporate evidence path |

> **Counsel tip:** Do **not** assume “corporate mailbox = all evidence.” Ask whether *guest* or *personal* identities were used during the matter window.

---

## Red flags suggesting multiple identities

- The custodian references “joining as a guest” in external Teams meetings.  
- Review set is missing Teams messages that others recall.  
- Emails reference OneDrive/SharePoint links, but **no copies** showed up.  
- Account had **server‑side forwarding** or **redirect** rules.  
- IT notes **legacy protocol** usage (IMAP/POP) or unusual mobile sign‑ins.  
- Name/domain changed (historic UPN likely exists).  
- Known collaboration with **vendors/co‑counsel** in shared project sites.

---

## What Identity Forensics adds (counsel‑readable steps)

1. **Account mapping** – Identify current UPN, historic UPNs, guest identities, and any personal MSA indicators.  
2. **Signal correlation** – Cross‑check Entra sign‑ins, Teams memberships (guest vs member), share‑link metadata, mailbox rules, and OAuth app grants.  
3. **Targeted scope** – Expand **only** where signals justify: extra Teams channels, SharePoint sites, historic mailboxes, or guest contexts.  
4. **Defensible export** – Produce time‑bounded CSV/JSON plus a **manifest** (hashes, tool versions, operator) and a **one‑page identity map**.

---

## Counsel checklist (what to ask at intake)

- **UPNs:** What’s the custodian’s current UPN? Any **historic** addresses?  
- **Guests:** Did they participate as a **guest** in partner Teams or sites? Which ones?  
- **Sharing:** Were files shared externally? What link types (specific‑people, people‑with‑link)?  
- **Rules:** Any forwarding/redirect rules to personal accounts?  
- **Devices:** Did they use **personal devices** or mobile apps for work content?  
- **OAuth:** Any connected third‑party apps (Box, Dropbox, Slack, etc.) during the period?  
- **Window:** Confirm **UTC** start/end; note holds and retention policies.

*(See `/method/intake-checklist.md` for the full list.)*

---

## Scope decisions (how we stay proportional)

- **Include:** identities/locations with **documented** activity during the date window (e.g., guest team where custodian posted files).  
- **Exclude (or defer):** personal accounts **without** corporate‑use signals.  
- **Document:** Every inclusion maps to an identity signal (defensibility).  
- **Bound:** All exports respect the counsel‑approved **UTC** window.

---

## Example counsel‑level language (for a meet‑and‑confer or letter)

> “The custodian acted under a primary work account, a historic alias following a domain change, and as a guest in a partner Team. Identity‑aware scoping is necessary to capture those Teams posts and associated SharePoint files. We will expand search locations to include the partner Team and related sites for the agreed date range, and will document each location’s basis in identity signals.”

---

## Deliverables you’ll receive

- **Identity Map (1 page)** – shows Work / Historic / Guest / (if relevant) Personal identities and where evidence sits.  
- **Added‑hits summary (CSV)** – new items found versus the default collection.  
- **Evidence bundle + manifest** – time‑bounded exports with hashes and operator/tool metadata.  
- **Two‑pager brief** – plain English explanation for partners/clients.

---

## Where this fits in your matter

- **Early Case Assessment:** quickly surface identity risks that can cause re‑collections.  
- **Collection Scoping:** lock in a precise, identity‑aware scope (Teams/SharePoint/Exchange).  
- **Pre‑Production QA:** verify there are no unexplained gaps tied to guest/personal identities.  
- **Lessons Learned:** recommend identity hygiene to reduce repeat risk.

---

**See also**  
- `/method/identity-forensics-method.md` – How the method runs  
- `/method/intake-checklist.md` – Questions that change scope  
- `/method/evidence-map-template.md` – One‑page identity map you’ll receive  
- `/examples/` – Short, redacted walk‑throughs for common gaps