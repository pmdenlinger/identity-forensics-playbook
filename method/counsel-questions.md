# Identity Forensics – Counsel Questions (Scoping Aid)

**Purpose:**  
These questions help litigation counsel and eDiscovery PMs identify the **identity‑driven risks** that can cause incomplete collections, missing Teams/OneDrive evidence, or gaps in audit trails.  
Use these questions during custodian interviews, calls with IT, early case assessment, or discovery planning.

These questions are intentionally **plain‑English**, and map directly to Identity Forensics workflows.

---

## 1) Names, Aliases, and Identity History

1. **Has the custodian ever changed their name** (marriage, legal change, preferred name) during the relevant period?  
2. **Has their email address or login changed** (UPN, domain migration, rebranding)?  
3. Are they known by **informal variations** of their name that might appear in Teams or email?

*Why this matters:* collection tools often miss historic UPNs or alias mailboxes unless explicitly added.

---

## 2) Accounts and Access Patterns

4. Does the custodian use **more than one account** to access work systems?  
   - Work account  
   - Guest accounts in partner/vendor/client tenants  
   - Personal Microsoft Account (MSA)  
   - Personal email (Gmail/iCloud/etc.)

5. Has the custodian ever accessed corporate systems from a **personal device** or **mobile app**?  
6. Does the custodian have access to any **shared mailboxes** or **departmental inboxes**?

*Why this matters:* identity mixing leads to Teams/SharePoint content being stored outside the custodian’s primary mailbox/OneDrive.

---

## 3) Teams and Collaboration Context

7. Which **Teams channels or projects** did the custodian work in during the matter period?  
8. Did they participate as a **Guest** in any external Teams channels (vendors, co‑counsel, clients)?  
9. Are there any **cross‑company** collaboration groups we need to account for?

*Why this matters:* Teams messages created under guest identities often do **not** appear in default tenant-only collections.

---

## 4) File Sharing and Document Handling

10. Has the custodian ever shared files with **external entities** (vendors, partners, co‑counsel)?  
11. Do they know whether files were shared via:  
    - **Specific‑people** links  
    - **People‑with‑link** (anonymous or semi-public)  
    - Direct attachments  
12. Did they regularly work in **SharePoint project sites**, or mostly attach items from their OneDrive?

*Why this matters:* external file shares often live in SharePoint project sites, not the custodian’s personal OneDrive.

---

## 5) Email Behavior and Rules

13. Has the custodian ever set up **auto‑forwarding**, **redirect**, or **BCC** rules?  
14. Do they send or receive sensitive data using **alternate mailboxes**?  
15. Did they delegate access to other team members (or receive delegated rights)?

*Why this matters:* forwarding rules may indicate evidence flowing to non‑standard repositories.

---

## 6) Applications, Integrations & OAuth Access

16. Does the custodian use any **third‑party apps** (Box, Dropbox, Slack, Notion, Trello) connected to their Microsoft 365 account?  
17. Have they used **mobile apps** that prompt for different identities (e.g., personal Outlook.com)?  
18. Have they installed any **productivity plugins** or browser extensions?

*Why this matters:* OAuth grants may allow external apps to access files silently.

---

## 7) Devices and Locations

19. Does the custodian use a **personal laptop or mobile device** for work?  
20. Have they worked while **traveling internationally**, or in locations that might trigger unusual sign‑ins?  
21. Have they ever accessed Teams/SharePoint via a **browser private mode** or alternate profile?

*Why this matters:* device identity changes affect audit visibility and can generate “missing messages.”

---

## 8) Retention, Holds, and Timing

22. When were **legal holds** applied (exact or approximate dates)?  
23. Were there any **retention policies** that could purge older content?  
24. Has the custodian ever **left the company**, been re‑hired, or transferred departments?

*Why this matters:* timing affects mailbox/OneDrive preservation, and formerly deprovisioned accounts may have lost data.

---

## 9) Known Pain Points or Red Flags

25. Any prior issues with:  
   - Account lockouts  
   - MFA resets  
   - Suspicious sign‑ins  
   - Lost or replaced devices?  
26. Has IT ever mentioned unusual access patterns?

*Why this matters:* identity anomalies can signal data that lives outside standard collections.

---

## 10) Counsel Summary Questions (Decision-Makers Only)

27. **If this custodian used multiple identities, which ones are “in scope” for this matter?**  
28. **Do we need to defensibly exclude personal accounts**, and if so, under what rationale?  
29. **What is the narrowest sufficient scope** that still captures all relevant activity?  
30. **Does the default search appear complete**, or do identity signals suggest expansion?

---

# How to Use This Checklist

- Use during **custodian interviews**, **ECA**, discovery planning, and kickoff calls with IT.  
- Answers feed directly into the **Identity Map** and **Evidence Scope**.  
- Keeps collections **defensible**, **complete**, and **proportional**.  
- Supports affidavits, declarations, and **search adequacy** arguments.

For visuals and example walk‑throughs, see `/examples/` in this repository.
