# Glean Salesforce — Documentation Footprint & Release Cadence

A research snapshot to size up Glean's investment on its Salesforce product line, for comparison against Microsoft's OOB Salesforce connector roadmap. Captured 2026-04-28.

All data points below were collected directly from `docs.glean.com` via Playwright (the site is a Docusaurus SPA — `Last updated` strings render after JS execution and are git-driven).

---

## Section 1 — Salesforce Documentation Pages (Last-Updated Timestamps)

Glean maintains **9 dedicated Salesforce pages** across the Connector and Actions sections of the docs site. Every page has been updated within the last ~60 days, indicating active maintenance rather than a write-once artifact.

| # | Page | Type | Last Updated |
|---|---|---|---|
| 1 | [SF connector overview](https://docs.glean.com/connectors/native/salesforce/about) | Concept + schema + ACL | **Mar 18, 2026** |
| 2 | [SF connector setup](https://docs.glean.com/connectors/native/salesforce/setup) | Deployment | **Apr 10, 2026** |
| 3 | [Use the SF connector](https://docs.glean.com/connectors/native/salesforce/use-salesforce-connector) | Hero scenarios | **Mar 25, 2026** |
| 4 | [Additional objects concepts](https://docs.glean.com/connectors/native/salesforce/additional-objects) | Custom / extended objects | Feb 27, 2026 |
| 5 | [SF attachments indexing](https://docs.glean.com/connectors/native/salesforce/salesforce-index-attachment) | Files & attachments | Mar 18, 2026 |
| 6 | [SF FAQ](https://docs.glean.com/connectors/native/salesforce/faq) | FAQ | Mar 13, 2026 |
| 7 | [SF troubleshooting](https://docs.glean.com/connectors/native/salesforce/troubleshooting) | Troubleshooting | Feb 27, 2026 |
| 8 | [Salesforce Search action](https://docs.glean.com/actions/datasource/salesforce/salesforce-search) | Action (NL → SOQL grounding) | Mar 17, 2026 |
| 9 | [Update SF Opportunity action](https://docs.glean.com/actions/datasource/salesforce/update-salesforce-opportunity) | Action (write-back) | Mar 25, 2026 |

**Observations**

- 9/9 pages updated in the last 60 days. The most recently touched page (`setup`, Apr 10, 2026) is only 18 days old at capture time.
- Dedicated pages exist for *both* surfaces: the connector (crawl/index/permissions) and Actions (real-time read + write-back). This is two separate product lines.
- Docusaurus exposes `Last updated` but not first-published date. The earliest visible reference (see Section 3) places the connector in active maintenance by **April 2025**, so SF has been GA earlier than that.

---

## Section 2 — Documented Hero Prompts (Audit List)

For full prompt-by-prompt traceability, see the companion file [glean-sf-prompts.md](glean-sf-prompts.md), which pairs each documented Glean prompt with its source URL.

---

## Section 3 — Salesforce Feature Releases (11-Month Window, 2025-04 → 2026-02)

Pulled from the [Glean Release Notes index](https://docs.glean.com/release-notes). 27 release notes were scanned; 9 contain *substantive* Salesforce-specific feature entries (occasional incidental mentions like "Simpplr migrating off Salesforce" are excluded).

| # | Release Date | Feature | FR / ROAD ID | Surface | Source |
|---|---|---|---|---|---|
| 1 | 2025-04-17 | Improvements to setup of Salesforce additional objects (self-serve) | FR-3263 | Connector | [release](https://docs.glean.com/release-notes/releases/2025-04-17-april-release) |
| 2 | 2025-04-30 | Continued iteration on additional-objects self-serve setup | FR-1302 | Connector | [release](https://docs.glean.com/release-notes/releases/2025-04-30-april-release) |
| 3 | 2025-05-20 | **Glean supports Salesforce SOQL actions** (NL + SOQL queries) | FR-2020 | Actions | [release](https://docs.glean.com/release-notes/releases/2025-05-20-may-release) |
| 4 | 2025-06-18 | **Update Salesforce Opportunity action** (write-back from within Glean) | FR-3170 | Actions | [release](https://docs.glean.com/release-notes/releases/2025-06-18-june-release) |
| 5 | 2025-07-16 | Glean Assist (admin console) customization for Zendesk, **Salesforce**, ServiceNow | FR-2811 | Assistant | [release](https://docs.glean.com/release-notes/releases/2025-07-16-july-release) |
| 6 | 2025-08-27 | **Assistant supports Salesforce Search with SOQL action** (NL → sort/filter on SF data) | FR-3888 | Assistant | [release](https://docs.glean.com/release-notes/releases/2025-08-27-august-release) |
| 7 | 2025-09-24 | **Salesforce connector now supports draft Knowledge articles** | FR-3649 | Connector | [release](https://docs.glean.com/release-notes/releases/2025-09-24-september-release) |
| 8 | 2026-01-28 | **Hybrid search for Salesforce dashboards & reports** (indexes dashboard metadata, runs live queries) | ROAD-761 | Connector / Agents | [release](https://docs.glean.com/release-notes/releases/2026-01-28-january-release) |
| 9 | 2026-02-25 | **Native support for additional Salesforce standard objects**: Contract, SBQQ_Quote__c, Product2, SBQQ_QuoteLine__c, SBQQ_Subscription__c, Order, Quote, OrderItem | ROAD-1093 | Connector | [release](https://docs.glean.com/release-notes/releases/2026-02-25-february-release) |

**Observations**

- Average cadence: **one major Salesforce-related shipment every ~5–6 weeks** over an 11-month window.
- Coverage spans **four product surfaces**: Connector, Actions, Assistant, Agents. SF FRs/ROAD IDs are spread across `FR-1026` to `FR-3888` and `ROAD-761`/`ROAD-1093`, indicating SF features are tracked as parallel streams in multiple roadmaps rather than a single isolated epic.
- Actions track (SOQL search + write-back) was already GA-quality by mid-2025. Microsoft does not have an architectural equivalent in OOB today (FCC is the closest path).
- The **2026-02-25** release alone added 8 standard objects natively, including the full SBQQ (Salesforce CPQ) family — closing what would otherwise be a major Tier-1 enterprise gap.

---

## Section 4 — Implications for Microsoft OOB Connector PMs

Headline: **Glean's Salesforce line ships at a cadence and breadth that implies a 1.5–3 PM-equivalent investment plus a dedicated tech-writer review loop**, on top of shared Connectors-platform, Actions-platform, and Assistant/Agents teams. The signals:

1. **9 dedicated docs pages, all maintained quarterly or sooner** — implies someone (PM or tech writer) owns the doc surface continuously.
2. **9 substantive feature ships in 11 months across 4 surfaces** — Connector, Actions, Assistant, Agents. Tracked under both `FR-` and `ROAD-` prefixes, suggesting at least two separate planning systems / product orgs touch SF.
3. **Hero scenarios documented for 3 distinct Glean surfaces** (Search, Assistant, Agents — see [glean-sf-prompts.md](glean-sf-prompts.md)) — each surface has its own GTM angle, which is typically owned by a dedicated PM.
4. **Industry benchmark for connector-centric companies** (Workato, Tray, Fivetran, Zapier): a Tier-1 SaaS connector (SF, ServiceNow, Workday) is staffed with 1 PM + 2–4 engineers; write-back / actions is usually a *separate* PM line because it adds OAuth, permissions, and write-audit complexity.

---

## Sources

- [Glean Salesforce connector docs](https://docs.glean.com/connectors/native/salesforce/about)
- [Glean Salesforce Search action docs](https://docs.glean.com/actions/datasource/salesforce/salesforce-search)
- [Glean Update Salesforce Opportunity action docs](https://docs.glean.com/actions/datasource/salesforce/update-salesforce-opportunity)
- [Glean Release Notes index](https://docs.glean.com/release-notes)
- Companion files: [glean-scorecard.html](glean-scorecard.html), [glean-sf-prompts.md](glean-sf-prompts.md)

Captured: 2026-04-28
