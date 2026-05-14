# Salesforce CRM Connector — Schema Editor

Interactive browser-based tool for reviewing and editing the Salesforce CRM Connector schema configuration.

## Usage

Visit: <https://kai-cloud.github.io/sf-schema-editor/>

## Eval Query Set (143 prompts)

### By Level

| Level | # | Description |
|---|---|---|
| Critical | 75 | Core search scenarios that must work |
| Expected | 41 | Common scenarios expected to work |
| Aspirational | 27 | Stretch scenarios (chatter, notes, transcripts, extended objects) |
| **Total** | **143** | |

### By Pattern

| Pattern | # | Query Index | Sample Query |
|---|---|---|---|
| Lookup | 7 | 6-10, 74, 112 | Pull up the account for Pinnacle Health Systems. |
| Field | 20 | 11-25, 117, 134-137 | What industry is Grand Hotels & Resorts Ltd in? |
| Filter | 27 | 1, 4-5, 26-29, 31, 33, 35, 41, 43-44, 46, 67, 71-72, 77, 80-81, 83, 138-143 | Which leads have a status of Working - Contacted? |
| Date | 9 | 36-40, 47-48, 65, 82 | What opportunities are closing in April 2026? |
| Numeric | 8 | 51-53, 56, 66, 68, 76, 84 | Which opportunities have a probability greater than 50%? |
| Aggregation | 5 | 54, 57-58, 69, 78 | What is the largest opportunity closed in June 2026 by dollar value? |
| Cross-object | 28 | 2-3, 30, 32, 34, 42, 45, 49-50, 55, 59-64, 70, 73, 75, 79, 113-114, 116, 118, 120-123 | Which contacts are linked to cases filed on GC5060 products? |
| Extended object | 24 | 85-87, 96-104, 106, 119, 124-133 | What campaigns are linked to our hot leads? |
| Unstructured data | 15 | 88-95, 105, 107-111, 115 | What chatter posts mention the United Oil renewal? |
| **Total** | **143** | | |

### By Feature Delivery

Counted by the latest feature each query depends on. Queries needing multiple features are counted only in the latest milestone row.

| Milestone | Feature | # | Query Index |
|---|---|---|---|
| M1 | Standard fields on Account, Lead, Contact, Opportunity, Case | 89 | 1-58, 60-62, 64-82, 84, 112-114, 117-118, 121-123 |
| M2 | Custom fields (`__c`) on the 5 core objects | 13 | 59, 63, 83, 134-143 |
| M3 | Case comments, attachments | 10 | 88-90, 107-111, 115, 120 |
| M4 | Events, Tasks (Activities) | 3 | 86-87, 116 |
| M5 | Campaign, Campaign Member | 11 | 85, 124-133 |
| M6 | Chatter feed item, Discussion forum | 6 | 91-95, 105 |
| M7 | Order, Order items | 3 | 99-101 |
| M8 | Product, Quote | 8 | 96-98, 102-104, 106, 119 |
| M9 | CPQ | 0 | — |
| M10 | Custom Objects | 0 | — |
| **Total** | | **143** | |

Source: [143-0512-seval-friendly-queryset.tsv](../SSP/20_SalesforceCC/03_Spec/04_Eval/20260512-SF-oob-custom-fcc-eval/143-0512-seval-friendly-queryset.tsv)

### Custom Fields (__c) Queried

13 of the 143 queries reference OOB sample-data-pack custom fields on the **Case** object:

| Query # | Prompt | Custom Field | Object |
|---|---|---|---|
| 59 | Which contacts are linked to cases filed on GC5060 products? | `Product__c` | Case |
| 63 | Which accounts have open cases with a potential liability flag? | `PotentialLiability__c` | Case |
| 83 | What are all the cases linked to the GC1020 product? | `Product__c` | Case |
| 134 | What is the product on case 00001001? | `Product__c` | Case |
| 135 | Is potential liability flagged on case 00001005? | `PotentialLiability__c` | Case |
| 136 | Was there an SLA violation on case 00001012? | `SLAViolation__c` | Case |
| 137 | What is the product on case 00001019? | `Product__c` | Case |
| 138 | Show me all cases on the GC1060 product. | `Product__c` | Case |
| 139 | Show me all cases on the GC3060 product. | `Product__c` | Case |
| 140 | Show me cases with SLA violations on the GC1060 product. | `SLAViolation__c`, `Product__c` | Case |
| 141 | List cases where SLA violation is No. | `SLAViolation__c` | Case |
| 142 | Which cases have BOTH SLA violation AND potential liability flagged? | `SLAViolation__c`, `PotentialLiability__c` | Case |
| 143 | Show me cases with potential liability on the GC3060 product. | `PotentialLiability__c`, `Product__c` | Case |
