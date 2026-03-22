# Identity Forensics – Evidence Map Template

**Purpose:**  
This template captures the **identity relationships**, **activity signals**, and **evidence locations** for a custodian.  
It is intended to be a *single‑page reference* for counsel, review teams, and technical operators, ensuring that all relevant identities and data sources are included in scope.

Populate one map per custodian **before** collections begin.

---

## 1) Custodian Overview

- **Custodian Name:**  
- **Role / Department:**  
- **Time Window (UTC):** From __ / __ / ____  To __ / __ / ____  
- **Legal Holds (if any):**  
- **Matter / Case ID:**  

---

## 2) Identity Inventory (Work, Historic, Guest, Personal)

Fill in every identity under which the custodian may have acted during the matter period.

| Identity Type | Identifier / UPN | Notes (When Used / Why Relevant) |
|---------------|------------------|----------------------------------|
| **Work (current)** | | Primary login; mailbox; Teams/SharePoint anchor |
| **Work (historic)** | | Name changes, domain migrations; may hold older messages/files |
| **Shared Mailboxes** | | Access rights? (FullAccess / SendAs / Delegate) |
| **Guest Accounts** | | Across partner/client/vendor tenants; Teams/SharePoint activity |
| **Personal MSA** | | Outlook.com/Hotmail; mobile use; link access; forwarding rules |
| **Other Personal Accounts** | | Gmail/iCloud if referenced in share links or rules |
| **Developer/Sandbox IDs** | | If relevant; may hold off‑tenant activity |

> **Goal:** Confirm which identities require evidence pulls or audit review.

---

## 3) Key Activity Signals (What shows this identity was used?)

Populate with signals collected from IT or audit exports.

| Signal Type | Evidence Source | Relevant Identity | Why It Matters |
|-------------|----------------|------------------|----------------|
| **Sign‑ins** | Entra ID logs | | Shows which identities were active; reveals guest/personal usage |
| **Teams Memberships** | Teams export | | Identifies channels where posts/files may reside |
| **Share/Link Metadata** | OneDrive/SharePoint | | Reveals external sharing; file access paths |
| **Mailbox Rules** | Exchange | | Detects forwarding/redirect/BCC (exfil indicators) |
| **OAuth Grants** | Graph API | | Detects 3rd‑party app access to mailbox/files |
| **Device Identity** | Device logs | | Shows unmanaged/mobile access patterns |

> **Goal:** Tie each identity to actual activity, not assumptions.

---

## 4) Evidence Locations (Teams, SharePoint, Exchange)

