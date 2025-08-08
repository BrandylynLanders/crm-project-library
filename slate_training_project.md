# Slate CRM Training Project: From Spreadsheet to Deliver Series
## Project Overview
This project organizes internal Slate CRM training content for both end users and admins using a structured spreadsheet format. It supports the creation of a searchable training library and delivery of learning content through Slate Deliver email campaigns.

The end goal is to evolve this model into a Slate dataset and potentially provide the community with a suitcase that includes:
- Sample dataset structure
- Deliver templates
- Campaign logic
- Workflow triggers (optional)

## Phase 1: Spreadsheet as Training Repository
| Element         | Description |
|----------------|-------------|
| Tabs           | User Training, Admin Training |
| Row Structure  | Each row = one step in a multi-step training |
| Key Columns    | Topic, Step Number, Step Description, Link, Screenshot, Effort Level, Notes, Category, Audience |
| Effort Levels  | Quick Win, Standard Task, Deep Dive |
| Use Cases      | Troubleshooting stuck applications, building queries, managing events, etc. |

## Phase 2: Slate Deliver Campaign
- Create a folder in Deliver named: Slate Training Series
- Design a repeating tokenized email template with:
  - Header: {{ topic }}
  - Body: loops through {{ steps }}, includes links and optional screenshots
  - Tags: Used for filtering topics by category or user type

Example layout:

### {{ topic }}

{{#each steps}}
**Step {{ step_number }}:** {{ step_description }}  
{{#if link}}[Related Resource]({{ link }}){{/if}}  
{{#if screenshot}}Screenshot: {{ screenshot }}{{/if}}

---
{{/each}}

## Phase 3: Long-Term Goal – Move to Slate Dataset
- Replace spreadsheet with a custom Dataset in Slate
- Fields: Topic, Step Number, Step Description, Link, Image, Effort Level, Tags
- Query-enabled for use in Portals or public-facing knowledgebase
- Integration options:
  - Portal page: Searchable training library
  - Deliver: Tokenized query-based email training
  - Scheduler: Tie trainings to onboarding events

## Future Ideas for the Slate Community
- Community-facing “Training Suitcase” with:
  - Sample dataset
  - Admin and user-focused Deliver templates
  - Scheduler template for live sessions
  - Sample Portal layout
- Deliver automation logic (triggers on user type, inactivity, etc.)
- Filters for “last updated,” “effort level,” or “category”

## Why This Project Matters

Slate CRM users need bite-sized, searchable, and context-aware training. By combining structured documentation with the flexibility of Deliver, this project turns training into a self-serve ecosystem that can grow with your institution — and be replicated elsewhere.
