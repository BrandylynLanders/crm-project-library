# 2. Queries

Queries are the **engine of Slate**. They drive reporting, Deliver (Email) campaigns, events, workflows, and populations.  
Because a single edit can disrupt communications or data flows, queries require **strict, risk‑based naming conventions**.

---
## 2.1 Core Principles for Query Naming

1. **Every query begins with a functional prefix**  
   - Communicates **purpose and risk** at a glance.  
   - Supports **safe editing, auditing, and role‑based permissions**.

2. **Include audience and/or division**  
   - Use the **standard audience codes** from Section 1.3.  
   - Combine with college/program code for clarity:  
     ```
     LIST_GR_FCOM_InterviewEligible_20250930
     ```

3. **Add a short, clear purpose**  
   - Use 1‑3 words to describe the query’s function.  
   - Avoid generic names like `Final`, `Test`, or `Copy of Query`.

4. **Add date if time‑sensitive**  
   - Use **YYYYMMDD** format for snapshots, event‑specific queries, or deliver mailings.  
   - Ensures **chronological sorting**.

5. **Archive or delete safely**  
   - Prefix with `Z_` or move to `Z_Archive` folder after a campaign cycle.

---
## 2.2 Query Prefixes and Their Purposes

| **Prefix** | **Purpose / Use Case**                                   | **Risk Level** |
|-----------|-----------------------------------------------------------|----------------|
| **QRY_**  | General ad hoc queries for reporting or reference          | Low            |
| **EXP_**  | Export queries for data extraction (CSV, Excel, JSON)      | Medium         |
| **LIST_** | Deliver / mailing list queries feeding email campaigns     | High           |
| **POP_**  | Population definition queries for workflows or dashboards  | High           |
| **COM_**  | Communications trigger queries for automated sends         | High           |
| **WFL_**  | Workflow trigger queries (app review, scoring, automation) | High           |
| **AUD_**  | Audience/portal access queries for portals or events       | Medium         |
| **EVT_**  | Event queries for communications and reporting             | Medium         |
| **REP_**  | Reporting queries feeding dashboards or reports            | Medium         |
| **TEST_** | Temporary or sandbox queries for testing logic             | Low            |

---

## 2.3 Query Naming Structure
