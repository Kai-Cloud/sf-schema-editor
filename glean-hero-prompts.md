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

## Glean Salesforce Actions — documented sample prompts

Source: [Glean: Salesforce Actions Index](https://docs.glean.com/actions/datasource/salesforce/sf-index)

**Remark:** Each Glean Salesforce Action has its own documentation page with sample prompts. These are purpose-built, prompt-ready CRM actions that enable write-back and workflow automation from Glean Assistant and Agents. Per-user OAuth to Salesforce is required.

| # | Action | Prompt (verbatim) | Source |
|---|---|---|---|
| 15 | Salesforce search | "What is the stage of the Acme opportunity?" | [Salesforce Search](https://docs.glean.com/actions/datasource/salesforce/salesforce-search) |
| 16 | Search with SOQL | "Total ARR of all the opportunities closed from June to August." | [Search with SOQL](https://docs.glean.com/actions/datasource/salesforce/search-salesforce-with-soql) |
| 17 | Create lead | "Create a new lead for ABC JIM, Director of Engineering at XYZ Inc, email abc@example.com, phone 444-555-1111, located in San Francisco. Set lead source to Trade Show." | [Create lead](https://docs.glean.com/actions/datasource/salesforce/create-lead) |
| 18 | Update lead | "Find the lead for ABC at XYZ Inc and update his status to Working - Contacted with a note that says Sent intro email about enterprise product demo." | [Update lead](https://docs.glean.com/actions/datasource/salesforce/update-lead) |
| 19 | Get lead | "Get the full details for Salesforce lead ID 00QPZ000001rbt8YAA." | [Get lead](https://docs.glean.com/actions/datasource/salesforce/get-lead) |
| 20 | Add lead to campaign | "Add lead ID 00QPZ000001rbt8YAA to the Q1 Product Launch campaign." | [Add lead to campaign](https://docs.glean.com/actions/datasource/salesforce/add-lead-to-campaign) |
| 21 | Create contact | "Check if a contact exists for abc@example.com. If not found, create a new contact for ABC JIM, Director of Product at XYZ Solutions." | [Create contact](https://docs.glean.com/actions/datasource/salesforce/create-contact) |
| 22 | Update contact | "Find the contact for abc@example.com and update her title to VP of Product, department to Product Management." | [Update contact](https://docs.glean.com/actions/datasource/salesforce/update-contact) |
| 23 | Get contact | "Get the full details for Salesforce contact ID 003PZ000001rbt8YAA." | [Get contact](https://docs.glean.com/actions/datasource/salesforce/get-contact) |
| 24 | Associate contact to account | "Link contact ID 003PZ000001rbt8YAA to account ID 001PZ000003xyzABC." | [Associate contact to account](https://docs.glean.com/actions/datasource/salesforce/associate-contact-to-account) |
| 25 | Create account | "Create a new Salesforce account for Abc Corporation with website abc.com." | [Create account](https://docs.glean.com/actions/datasource/salesforce/create-account) |
| 26 | Get account | "Get the full details for Salesforce account ID 001PZ000003xyzABC." | [Get account](https://docs.glean.com/actions/datasource/salesforce/get-account) |
| 27 | Create opportunity | "Create a new opportunity for ABC Corp Enterprise License, amount $150,000, close date March 31, stage Qualification." | [Create opportunity](https://docs.glean.com/actions/datasource/salesforce/create-opportunity) |
| 28 | Update opportunity | (use-case descriptions only, no verbatim prompt) | [Update opportunity](https://docs.glean.com/actions/datasource/salesforce/update-salesforce-opportunity) |
| 29 | Get opportunity | "Get the full details for Salesforce opportunity ID 006PZ000003xyzABC." | [Get opportunity](https://docs.glean.com/actions/datasource/salesforce/get-opportunity) |
| 30 | Create campaign | "Create a new campaign called 'Q1 2024 Product Launch' with type 'Email' and status 'Planned'." | [Create campaign](https://docs.glean.com/actions/datasource/salesforce/create-campaign) |
| 31 | Add contact to campaign | "Add contact ID 003PZ000001rbt8YAA to the Q1 Product Launch campaign." | [Add contact to campaign](https://docs.glean.com/actions/datasource/salesforce/add-contact-to-campaign) |
| 32 | Send email | "Find the lead for ABC JIM at XYZ Corp, send her a personalized introduction email with subject Partnership Opportunity, and update her lead status to Working." | [Send email](https://docs.glean.com/actions/datasource/salesforce/send-email) |
| 33 | Log email activity | "Log the follow-up email I sent to abc@example.com about Case 00001234 with subject Re: Technical Issue Resolution." | [Log email activity](https://docs.glean.com/actions/datasource/salesforce/log-email-activity) |
| 34 | Create call log | "Log a call for the Opportunity XYZ Corp Q1 Deal with subject Discovery Call, type Outbound, duration 30 minutes." | [Create call log](https://docs.glean.com/actions/datasource/salesforce/call-log) |
| 35 | Complete task | "Mark task 00T5g00007ABCDEFUA2 as completed with notes 'Spoke with prospect, confirmed needs, scheduled demo'." | [Complete task](https://docs.glean.com/actions/datasource/salesforce/complete-tasks) |
| 36 | Create note | "Find the Opportunity for XYZ Corp renewal and create a note summarizing the key points from today's call." | [Create note](https://docs.glean.com/actions/datasource/salesforce/create-note) |
| 37 | Get user info | "Get information about the current authenticated Salesforce user including their permissions." | [Get user info](https://docs.glean.com/actions/datasource/salesforce/get-user-info) |

## Live Mode / data fetching — claims without verbatim prompts

Source: [Glean: Salesforce connector — Data crawling and indexing and Data fetching](https://docs.glean.com/connectors/native/salesforce/about#data-crawling-and-indexing-and-data-fetching)

**Remark:** Glean documents Live Mode (per-user OAuth, real-time API fetch) for reports and dashboards, and a "Update Salesforce Opportunity" write-back action, but does not publish verbatim example prompts for these. Capabilities listed without prompts:

- Real-time fetch of report values and dashboard state to ground Assistant answers.
- Live read of newly created records before the next sync (e.g., an opp created moments ago).
- Write-back action: "Update Salesforce Opportunity" (stage, amount, close date, etc.) invoked from Assistant or Agents, gated by action-level RBAC and user OAuth.
- Pipeline hygiene agent and support triage agent workflows (described conceptually, no quoted prompts).
