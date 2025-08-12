# Slate File Naming Guide

**Section 1: General Principles**  
These principles apply to **all Slate assets** (Queries, Deliver/Email, Events, Forms, Portals, Organizations) before applying **module-specific naming rules**.

---
## 1.1 Folders Are for Humans; File Names Are for Systems
- **Folders:** Use **full, descriptive names** that are easy for new staff to understand.  
  - Example: `UG College of Business`, `GR School of Pharmacy`  
- **Files:** Use **prefixes, codes, and dates** to sort, filter, and search efficiently.

---
## 1.2 Use Underscores `_` Instead of Spaces or Dashes
- **Avoid spaces**  
  In exports and downstream automations, spaces are frequently used as split characters. This means file names can be **cut at the first space** (or everything after the space becomes a separate column/token), causing lost or misread suffixes like dates or sequence numbers. In portals/URLs, spaces are encoded as `%20`, which makes links longer, harder to read, and more brittle in copy/paste.

- **Avoid dashes `-`**  
  Slate search treats dashes as word breaks, which can fragment your terms. Dashes also get URL-encoded in some contexts, increasing the chance of broken or ugly links.

- **Prefer underscores `_`**  
  Underscores are URL-safe, predictable for Liquid parsing (e.g., `split: '_'`), and keep the full name intact during exports and when embedded in portals/links.

### Search behavior in Deliver (important)
- **Underscore caveat:** Deliver’s native search matches contiguous text. An underscore is not a space, so partial, spaced queries won’t match. For example, searching `Welcome 01` will **not** find `Welcome_01`.
- **Why underscores still help:** They create reliable **tokens** you can target to isolate groups:
  - `EMAIL_UG_` → all Undergraduate emails  
  - `_COB_` → all College of Business items  
  - `_01_` → all first-send messages in a sequence  
  - `EMAIL_GR_CPHS_` → Graduate, CPHS only
- **Team tip:** Teach users to search by **left-to-right tokens** you standardize in names:  
  `PREFIX_AUDIENCE_UNIT_CAMPAIGN_SEQ_Description_Date`  
  Example query strings your team can type: `EMAIL_UG_`, `EMAIL_GR_CPHS_`, `_Applicant_01_`.

This keeps exports clean, portal links stable, and day-to-day filtering practical—even with Deliver’s exact-match search behavior.

---
## 1.3 Include Audience and Division
Use **short, consistent codes** to identify who the item applies to.  
Combine audience with **program/college code** for specificity.

### **Standard Audience Codes**
UG = Undergraduate  
GR = Graduate  
ADP = Adult Programs  
NDS = Non-Degree Seeking  
INTL = International  
PAR = Parents / Guardians  
HSC = High School Counselors  
EMP = Employers / Corporate  
INT = Internal (Staff / Faculty)  
UNI = All-University  

### **Combine with Division or Program**
- `GR_FCOM` = Graduate – Frist College of Medicine  
- `GR_CPHS` = Graduate – College of Pharmacy & Health Sciences  
- `UG_COB`  = Undergraduate – College of Business  

---
## 1.4 Use Dates for Sorting and Version Control
- Append **YYYYMMDD** to items that repeat or are time-sensitive.  
- Ensures **chronological sorting** in Slate’s flat folder structure.  
- Example:  
GR_FCOM_CampusTour_20250926  
EMAIL_UG_COB_Yield_01_Welcome_20250805

---
## 1.5 Use Two- or Three-Digit Sequence Numbers for Multi-Step Processes
When naming files for campaigns, email series, or other multi-step processes, always use **leading zeros** (`01`, `02`, `03` or `001`, `002`, `003`).  

### Why Not Just “1, 2, 3”?
Slate sorts files **alphanumerically**, not numerically.  
If you use single digits, your files will sort like this:  
```
1, 10, 11, 2, 3, 4...
```
instead of the correct order:  
```
01, 02, 03, 04, 05...
```  

Using two or three digits ensures that steps stay in the correct sequence regardless of how many total steps are in the series.  
- **Two digits** (`01–99`) are sufficient for most campaigns.  
- **Three digits** (`001–999`) are helpful for very large projects or system-generated exports.

**Example Using Provided Table:**  
| AUDIENCE CODE | UNIT OR PROGRAM | Campaign  | Sequence# | Description         |  
|---------------|-----------------|-----------|-----------|---------------------|  
| UG            | FCOM            | Applicant | 01        | App Submitted       |  
| GR            | CPHS            | Inquiry   | 02        | Discover Belmont    |  
| ADP           | COB             | PostApp   | 03        | Check your portal   |  
| NDS           | MAEMI           | Awareness | 04        | Why Belmont         |  
| INTL          | CMPA            | Admitted  | 05        | Congratulations     |  

**How This Looks in a Slate File Name:**  
EMAIL_UG_FCOM_Applicant_01_AppSubmitted_20250805  
EMAIL_GR_CPHS_Inquiry_02_DiscoverBelmont_20250805  
EMAIL_ADP_COB_PostApp_03_CheckYourPortal_20250805  
EMAIL_NDS_MAEMI_Awareness_04_WhyBelmont_20250805  
EMAIL_INTL_CMPA_Admitted_05_Congratulations_20250805

---
## 1.6 Archiving & Cleanup
- Prefix retired items or folders with `Z_` or move to a `Z_Archive` folder.  
- Optionally create **annual archive folders** to manage volume.  
- Examples:  
Z_Archive_2024  
Z_UG_COB_Yield_2023

---
## 1.7 Intentional Prefixing to Communicate Risk
- **High-risk items** (operational queries, live mailing lists) must have **prefixes** to prevent accidental edits.  
- **Low-risk items** (ad hoc queries, testing) can have simple prefixes like `QRY_` or `TEST_`.

**Training Shortcut:**  
- ✅ Safe to edit: `QRY_`, `TEST_`  
- ⚠ Ask first: `LIST_`, `COM_`, `WFL_`, `POP_`, `EMAIL_`

---
**Next Sections:**  
- Module-Specific Naming Rules for  
- [Queries](Queries.md)  
- [Deliver / Email](Deliver_Email.md)  
- [Events](Events.md)  
- [Forms](Forms.md)  
- [Portals](Portals.md)  
- [Organizations](Organizations.md) 
