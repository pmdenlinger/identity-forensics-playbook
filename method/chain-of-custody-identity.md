# Identity Forensics – Chain of Custody (Identity-Aware)

**Purpose:**  
Identity Forensics (IF) produces evidence from multiple identity contexts (work UPN, historic UPNs, guest accounts, personal MSA indicators, OAuth tokens, device identities).  
This document defines how to preserve, track, and document the **chain of custody** for these identity-derived evidence sources so they are **admissible, defensible, and reproducible**.

The goal is simple: every item in the evidence bundle can be traced to  
**(1) who exported it, (2) from which identity context, (3) through which method, and (4) with what integrity protections.**

---

# 1) Scope of Chain of Custody

This procedure applies to all evidence produced by Identity Forensics, including:

- `signin_attribution.csv`  
- `teams_memberships.csv`  
- `share_links.csv`  
- `mailbox_rules.json`  
- `oauth_grants.json`  
- `teams_messages_expanded.csv`  
- `sharepoint_files_expanded.csv`  
- `added_hits_summary.csv`  
- `identity_map.png`  
- `manifest.json`  

Each file must be:

1. **Traceable** to a specific identity signal, query, or export.  
2. **Time‑bounded** to the approved matter window.  
3. **Cryptographically hashed** (SHA‑256).  
4. **Recorded** in a manifest with operator, tool versions, and timestamps.  
5. **Stored immutably** within the case evidence folder.

---

# 2) Evidence Directory Structure

Every Identity Forensics evidence bundle must follow this standardized structure: