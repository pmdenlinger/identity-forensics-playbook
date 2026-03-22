# Identity Forensics – Method (Playbook)

**Purpose.**  
Identity Forensics (IF) is a repeatable method to map a custodian’s **multiple digital identities** (work UPN, historic aliases, guest accounts, personal MSA, mobile tokens) and correlate those identities with **Microsoft 365** (and adjacent) activity signals. The goal is a **defensible, complete collection scope** and a clear, counsel‑readable evidence bundle—so cases don’t suffer re‑collections, schedule slips, or search‑adequacy challenges.

This document defines **roles, inputs, workflow, outputs, quality gates, privacy controls, and acceptance criteria** for running IF on a matter.

---

## 1) When to run Identity Forensics

Run IF whenever you see one or more of the following:

- **Teams/OneDrive gaps**: emails or testimony reference messages/files that don’t appear in default exports.  
- **Alias churn**: the custodian has historic UPNs, name changes, or migrated domains.  
- **Guest collaboration**: the custodian participated in **external** Teams or accessed partner SharePoint.  
- **Personal account hints**: forwarding rules, “sent from my phone” anomalies, or mobile‑only behavior.  
- **OAuth/legacy paths**: third‑party app grants or IMAP/POP usage that weaken audit visibility.

---

## 2) Roles & RASCI

- **Counsel / Litigation Lead (A/R)**: Defines date range, approves scope, owns legal defensibility.  
- **eDiscovery PM (A)**: Runs this method, tracks chain of custody, coordinates collections & review.  
- **Technical Operator (R)**: Executes queries/scripts, exports evidence, produces manifests & hashes.  
- **Client IT / M365 Admin (S/C)**: Provides exports (sign‑ins, memberships, share links, mailbox rules).  
- **Security / Compliance (S)**: Clarifies Conditional Access, DLP, retention/holds that affect visibility.

*(R = Responsible, A = Accountable, S = Support, C = Consulted)*

---

## 3) Inputs (What you need to start)

- **Matter details**: Case ID, custodian list, **time window** (UTC start/end), legal holds.  
- **Custodian identity basics**: current UPN, known aliases, name history, role/department.  
- **Tenant refs**: home tenant info, known **partner tenants**, any **dev/sandbox** tenants.  
- **Initial exports** (or permissions to pull):
