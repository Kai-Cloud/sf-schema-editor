# Salesforce CRM Connector — Schema Editor

Interactive browser-based tool for reviewing and editing the Salesforce CRM Connector schema configuration.

## Usage

Visit: <https://kai-cloud.github.io/sf-schema-editor/>

## Eval Query Set (111 prompts)

| Pattern | # | Query Index | Sample Query |
|---|---|---|---|
| List | 5 | 1-5 | Show me the top 50 accounts. |
| Lookup | 5 | 6-10 | Pull up the account for Edge Communications. |
| Field | 15 | 11-25 | What industry is Grand Hotels & Resorts Ltd in? |
| Filter | 22 | 26-35, 41-46, 49-50, 55-56, 67, 70-72, 76, 81 | Show me all accounts in the Energy industry. |
| Date | 9 | 36-40, 47-48, 65, 82 | What opportunities are closing in April 2026? |
| Numeric | 8 | 51-53, 66, 68, 73, 77, 84 | Which opportunities have a probability greater than 50%? |
| Aggregation | 9 | 54, 57-58, 69, 78 | What is the largest closed opportunity by dollar value? |
| Cross-object | 10 | 59-64, 74-75, 79, 83 | Which contacts are linked to cases filed on GC5060 products? |
| Extended object | 13 | 80, 85-87, 96-104, 106 | What campaigns are linked to our hot leads? |
| Custom objects | 0 | — | — |
| Unstructured data | 14 | 88-95, 105, 107-111 | What chatter posts mention the United Oil renewal? |
| **Total** | **111** | | |

Source: [eval-queryset-111.csv](../10_SSP/20_SalesforceCC/03_Spec/04_Eval/20260427-SF-oob-glean-eval/eval-queryset-111.csv)
