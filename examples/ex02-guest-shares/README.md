# EX02 – Guest‑Share Links: Identity Forensics for External File Access

**Scenario:**  
Reviewers notice missing documents referenced in conversations and emails. Purview collections for the custodian’s mailbox and OneDrive return **no copies** of files sent externally. Identity Forensics reveals the custodian used **share links**—including *external* and *specific‑people* shares—to provide access to people **outside the tenant**, meaning the original documents may not reside solely in the custodian’s OneDrive anymore.

This example shows how **Guest‑Share analysis** expands the evidence set beyond default Purview scopes by mapping **external recipients**, **share link types**, and **associated identity contexts**, ensuring litigation teams collect *everything the custodian exposed*.

---

## 🔎 Symptom (from counsel or review team)

- OneDrive file references appear in emails, but **files are missing** from the review set.  
- External parties confirm receiving files, yet **no copies appear** under the custodian’s OneDrive export.  
- Counsel suspects documents were shared with **vendors**, **co‑counsel**, or **partners**, but **can’t trace where the files went**.

**Hypothesis:**  
Default collection only targeted the custodian’s mailbox and OneDrive, but key files were accessed via **external guest identities** or **public/specific‑people share links**, not stored in local folders.

---

## 🧭 Identity Forensics Approach (high level)

1) **Extract share‑link metadata** from OneDrive/SharePoint:
   - Link type (anonymous / people‑with‑link / specific‑people / internal / expired)
   - Recipient identities (internal UPNs, guest UPNs, personal addresses)
   - Access timestamps

2) **Map external identities** involved in access:
   - Guest accounts (B2B collaboration)
   - Personal MSA/Google accounts used for link access
   - External partner domains

3) **Trace file lineage**:
   - Confirm whether external users downloaded, edited, or re‑shared files.
   - Identify files whose *primary* working copy is no longer in custodian’s OneDrive.

4) **Expand Purview / collection scope**:
   - Add SharePoint site(s) storing collaborative versions
   - Include external‑tenant evidence (where possible)
   - Collect linked Teams conversations referencing the documents

---

## 🧪 Included synthetic files (in this example folder)