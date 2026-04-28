# Glean Salesforce — Documented Hero Prompts

All prompts are quoted verbatim from Glean's official documentation, with source links for audit.

## A. Glean Salesforce Connector — Documented Prompts

Source: [Use the Salesforce Connector](https://docs.glean.com/connectors/native/salesforce/use-salesforce-connector)

| # | Prompt | Context | Source |
|---|---|---|---|
| A1 | "open cases for Acme in the last 30 days" | Faceted search filter | [src](https://docs.glean.com/connectors/native/salesforce/use-salesforce-connector) |
| A2 | "opportunities in stage Negotiation closing this quarter" | Faceted search filter | [src](https://docs.glean.com/connectors/native/salesforce/use-salesforce-connector) |
| A3 | "Acme – Q3 expansion" | Live-mode: recent opportunity lookup | [src](https://docs.glean.com/connectors/native/salesforce/use-salesforce-connector) |
| A4 | "open P1 cases for Contoso created today" | Live-mode: real-time case list | [src](https://docs.glean.com/connectors/native/salesforce/use-salesforce-connector) |
| A5 | "Show the top 10 opportunities closing this quarter by amount, with owner and stage." | Glean Assistant — top-N ranking | [src](https://docs.glean.com/connectors/native/salesforce/use-salesforce-connector) |
| A6 | "List escalated cases for Contoso created this week, with subject, status, and owner." | Glean Assistant — filtered case list | [src](https://docs.glean.com/connectors/native/salesforce/use-salesforce-connector) |

## B. Glean Salesforce Search (Action) — Documented Prompts

Source: [Salesforce Search action](https://docs.glean.com/actions/datasource/salesforce/salesforce-search)

| # | Prompt | Scenario | Source |
|---|---|---|---|
| B1 | "What is the stage of the Acme opportunity?" | Opportunity Status | [src](https://docs.glean.com/actions/datasource/salesforce/salesforce-search) |
| B2 | "Who is the CSM for the Acme account?" | Custom Object Lookup | [src](https://docs.glean.com/actions/datasource/salesforce/salesforce-search) |
| B3 | "Total ARR of all the opportunities closed from June to August." | Aggregation | [src](https://docs.glean.com/actions/datasource/salesforce/salesforce-search) |
| B4 | "What are the use cases associated with the Acme account?" | Use Case Association | [src](https://docs.glean.com/actions/datasource/salesforce/salesforce-search) |

---

**Total: 10 documented prompts** (6 from connector docs, 4 from Search action docs).

Retrieved: 2026-04-28
