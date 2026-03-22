# Identity Forensics – Intake Checklist (Counsel + eDiscovery PM)

This checklist gathers the information required to run **Identity Forensics (IF)** on any custodian.  
Use it during matter kickoff, custodian interviews, or early conversations with IT.

The goal: ensure that **all identities**, **all collaboration contexts**, and **all evidence locations** tied to the custodian are accounted for **before** collections begin.

---

## 1) Custodian Basics (Counsel / PM)

1. **Full legal name:**  
2. **Known prior names / spellings / aliases:**  
3. **Job title(s) during the matter period:**  
4. **Department / team(s):**  
5. **Manager(s) during matter period:**  
6. **Employment dates relevant to the case:**  

---

## 2) Identity & Account Information

7. **Current work UPN (login):**  
   - Example: `alex.smith@contoso.com`

8. **Historic UPNs / aliases:**  
   - Domain migrations, name changes, rebrands  
   - Example: `alex.s@oldcontoso.com`

9. **Secondary mailboxes / shared mailboxes:**  
   - Finance, sales ops, matter-specific shared mailboxes  
   - Access level (FullAccess / SendAs / Delegation)

10. **Guest accounts (B2B external):**  
    - Any partner/vendor/client tenants where custodian had a **Guest** role  
    - Names of partner organizations (if known)

11. **Personal Microsoft Account (MSA) usage:**  
    - Used on work devices?  
    - Used to access corporate Teams/SharePoint links?  
    - Any evidence of forwarding rules to personal Outlook.com?

12. **Other personal accounts used for work:**  
    - Gmail, iCloud, Yahoo, etc.  
    - Seen in share-link metadata, forwarding rules, or email headers?

13. **Developer / sandbox tenants:**  
    - Any accounts used for testing, demos, or dev environments?

---

## 3) Collaboration Context

14. **Teams involvement:**  
    - Internal teams/channels  
    - External/partner teams (Guest role)  
    - Any known “project workspaces” or cross-company teams?

15. **SharePoint / OneDrive activity:**  
    - Project sites  
    - Departmental sites  
    - Personal OneDrive activity patterns  
    - External sharing history?

16. **Known external sharings:**  
    - Files shared with vendors, co-counsel, partners  
    - Link types used (anonymous, specific people, internal-only)

17. **Devices used to access Teams/OneDrive:**  
    - Corporate laptop?  
    - Mobile apps?  
    - Unmanaged personal devices?

---

## 4) Email Behavior

18. **Forwarding rules (server-side):**  
    - Auto-forward, redirect, or BCC to other accounts

19. **Delegations:**  
    - Delegate access to/from teammates  
    - Service accounts or departmental inboxes

20. **Legacy authentication usage (if known):**  
