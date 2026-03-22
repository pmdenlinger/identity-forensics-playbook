# EX01 – Teams Gap: Identity Forensics Corrects an Incomplete Collection

**Scenario:**  
Counsel believes a custodian’s Microsoft Teams conversations are missing from the review set. Default collection targeted only the custodian’s *primary work mailbox/UPN*. Identity Forensics reveals the custodian also used (a) an **old/historic UPN**, (b) a **guest account** in a partner tenant, and (c) a personal **Microsoft Account (MSA)** on an unmanaged mobile device—creating collection blind spots.

**What this example shows (1 minute):**
- How to **attribute** the custodian’s identities (work, historic, guest, personal)  
- How to **expand scope** to capture Teams/SharePoint/OneDrive evidence tied to those identities  
- What **artifacts** to export for counsel (identity map, evidence manifest, added hits)

---

## 🔎 Symptom (as reported by counsel / review team)

- Teams threads referenced in email are **not present** in the export.
- OneDrive files shared in the chat are **missing** from review.
- The custodian says they “sometimes joined with a different account” during external meetings.

**Hypothesis:** Default collection limited to `alex.smith@contoso.com` (work UPN) missed evidence posted via **guest** identity and/or content linked to a **historic UPN** or **personal MSA** on mobile.

---

## 🧭 Identity Forensics Approach (high level)

1) **Map identities** for the custodian:
   - Primary work Entra ID UPN
   - Historic UPN(s) (e.g., name changes, domain migrations)
   - Guest account(s) in external tenants (B2B collaboration)
   - Personal Microsoft Account (MSA) evidence (tokens on unmanaged mobile)

2) **Trace activity** across Teams/SharePoint/OneDrive:
   - Entra ID Sign‑in patterns (apps, devices, tenants)
   - Teams team/channel memberships (including *Guest*)
   - Share/Link types (People with the link / Specific people / External)
   - Mailbox server‑side rules (for exfil indicators)

3) **Expand collection scope** (Purview Content Search, Compliance, or vendor tool):
   - Include historic UPNs, guest IDs, relevant Team/SharePoint sites
   - Pull additional Teams messages + linked files
   - Export with **manifest** (hashes, sources, time range, operator)

---

## 🧪 What you can run in this example (synthetic data)

> This folder contains redacted/synthetic inputs so you can **see** the workflow and **compare** expected outputs without needing live tenant access.

**Files**