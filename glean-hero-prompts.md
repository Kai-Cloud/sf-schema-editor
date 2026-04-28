# Glean Salesforce Connector — Hero User Prompts

## Synced connector only (pure indexed mode)

Source: [Glean: Use Salesforce Connector](https://docs.glean.com/connectors/native/salesforce/use-salesforce-connector)

| # | Prompt (verbatim) | Source |
|---|---|---|
| 1 | "open cases for Acme in the last 30 days" | [Use Salesforce Connector](https://docs.glean.com/connectors/native/salesforce/use-salesforce-connector) |
| 2 | "opportunities in stage Negotiation closing this quarter" | [Use Salesforce Connector](https://docs.glean.com/connectors/native/salesforce/use-salesforce-connector) |
| 3 | "open P1 cases for Contoso created today" | [Use Salesforce Connector](https://docs.glean.com/connectors/native/salesforce/use-salesforce-connector) |

## Synced connector + Glean Assistant actions

Source: [Glean: Use Salesforce Connector](https://docs.glean.com/connectors/native/salesforce/use-salesforce-connector)

| # | Prompt (verbatim) | Source |
|---|---|---|
| 4 | "Show the top 10 opportunities closing this quarter by amount, with owner and stage." | [Use Salesforce Connector](https://docs.glean.com/connectors/native/salesforce/use-salesforce-connector) |
| 5 | "List escalated cases for Contoso created this week, with subject, status, and owner." | [Use Salesforce Connector](https://docs.glean.com/connectors/native/salesforce/use-salesforce-connector) |

## Customer Briefing / Account Summary — related prompts

Source: [Glean Prompt Library](https://www.glean.com/prompt-library)

**Remark:** None of these are Salesforce-connector-only. They are blended scenarios that combine SF data with Gmail, Slack, Gong, Confluence, Google Drive, and similar sources. Glean does not publish a single canonical "Customer Briefing" or "Account Summary" prompt scoped to the SF connector alone.

| # | Title | Prompt (verbatim) | Source |
|---|---|---|---|
| 6 | Prepare for a customer presentation | "Prepare for a customer presentation and identify potential questions." | [Glean Prompt Library](https://www.glean.com/prompt-library) |
| 7 | Target Account Research | "Analyze specific articles regarding a company that a sales representative can use in personalized outreach." | [Glean Prompt Library](https://www.glean.com/prompt-library) |
| 8 | Recap recent customer meetings | "Summarize recent customer meetings including who attended and the topics that were discussed." | [Glean Prompt Library](https://www.glean.com/prompt-library) |
| 9 | Catch up on deal progression | "Create an overview of progress on a deal and summarize the latest requests." | [Glean Prompt Library](https://www.glean.com/prompt-library) |
| 10 | Creating Agendas for a Customer Meeting | "Create customer specific agendas for your regular touchbase." | [Glean Prompt Library](https://www.glean.com/prompt-library) |

## Glean Salesforce Search action (SOQL + indexed blend)

Source: [Glean: Salesforce Search action](https://docs.glean.com/actions/datasource/salesforce/salesforce-search)

**Remark:** These prompts require the "Search Salesforce with SOQL" action enabled. They are not served from the synced index alone — Glean translates the prompt to SOQL and queries Salesforce live, then blends results with the indexed corpus. Per-user OAuth to Salesforce is required.

| # | Category | Prompt (verbatim) | Source |
|---|---|---|---|
| 11 | Opportunity Status | "What is the stage of the Acme opportunity?" | [Salesforce Search action](https://docs.glean.com/actions/datasource/salesforce/salesforce-search) |
| 12 | Custom Object Lookup | "Who is the CSM for the Acme account?" | [Salesforce Search action](https://docs.glean.com/actions/datasource/salesforce/salesforce-search) |
| 13 | Aggregation | "Total ARR of all the opportunities closed from June to August." | [Salesforce Search action](https://docs.glean.com/actions/datasource/salesforce/salesforce-search) |
| 14 | Use Case Association | "What are the use cases associated with the Acme account?" | [Salesforce Search action](https://docs.glean.com/actions/datasource/salesforce/salesforce-search) |

## Live Mode / data fetching — claims without verbatim prompts

Source: [Glean: Salesforce connector — Data crawling and indexing and Data fetching](https://docs.glean.com/connectors/native/salesforce/about#data-crawling-and-indexing-and-data-fetching)

**Remark:** Glean documents Live Mode (per-user OAuth, real-time API fetch) for reports and dashboards, and a "Update Salesforce Opportunity" write-back action, but does not publish verbatim example prompts for these. Capabilities listed without prompts:

- Real-time fetch of report values and dashboard state to ground Assistant answers.
- Live read of newly created records before the next sync (e.g., an opp created moments ago).
- Write-back action: "Update Salesforce Opportunity" (stage, amount, close date, etc.) invoked from Assistant or Agents, gated by action-level RBAC and user OAuth.
- Pipeline hygiene agent and support triage agent workflows (described conceptually, no quoted prompts).
