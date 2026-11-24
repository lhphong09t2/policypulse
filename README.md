# PolicyPulse for Confluence Cloud — Interactive Forge Preview

**Live Interactive Preview:** [https://lhphong09t2.github.io/policypulse/](https://lhphong09t2.github.io/policypulse/)

Interactive UI prototype for **PolicyPulse**, a lightweight, zero-egress **Atlassian Forge** app (`"Runs on Atlassian"` · Forge SQL/KVS · `0` external data egress) built for bulk SOP read confirmations and deterministic **ISO/IEC 27001:2022 Clause 7.3 / SOC 2 CC1.4** audit evidence in Confluence Cloud.

## Interactive Workflows Included

1. **1-Click Bulk Policy Pack Assigner (`confluence:spacePage`)**
   - Assign target Confluence groups (e.g., `@all-employees`) and SLA due dates across an entire Space page hierarchy or CQL label (`label = "iso27001-mandatory"`) in a single click — without inserting per-page macros or bumping page version history across 20+ SOPs.
2. **Native Page Byline Receipt & Smart Revision Guard (`confluence:contentBylineItem`)**
   - Top-of-page attestation banner recording `Atlassian_Account_ID`, `Signed_Version`, `Acknowledged_UTC`, and tamper-evident `Receipt_SHA256`.
   - **Major-Version Only Guard:** Minor typo/formatting updates (`v3.0 -> v3.1`) preserve existing valid employee sign-offs, while major policy revisions (`v3.0 -> v4.0`) automatically re-request attestation.
3. **ISO 27001 Clause 7.3 & SOC 2 CC1.4 Auditor Matrix (`confluence:globalPage`)**
   - Real-time acknowledgment KPIs, status/department filters (`Acknowledged`, `Pending`, `Overdue`), 1-click overdue nudges, and deterministic CSV evidence export ready for Stage 2 / surveillance audit sampling.

## Privacy & Preview Architecture

- **100% Self-Contained Static Preview:** Zero external CDN dependencies, analytics, or network egress. All records shown in the preview (`@vanta-fin.io`) are synthetic demonstration fixtures.
- **Target Production Runtime:** Serverless Atlassian Forge (`confluence:spacePage`, `confluence:contentBylineItem`, `confluence:globalPage`) storing attestation records natively inside Atlassian-hosted Forge SQL.
