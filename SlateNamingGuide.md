# Slate File Naming Guide  
**Section 1: General Principles**

These principles apply to **all Slate assets** (Queries, Deliver/Email, Events, Forms, Portals, Organizations)
before applying **module-specific naming rules**.

---
## 1.1 Folders Are for Humans; File Names Are for Systems
- **Folders:** Use **full, descriptive names** that are easy for new staff to understand.  
  - Example: `UG College of Business`, `GR School of Pharmacy`  
- **Files:** Use **prefixes, codes, and dates** to sort, filter, and search efficiently.

---
## 1.2 Use Underscores `_` Instead of Spaces or Dashes
- **Avoid spaces** → can cause truncation in exports or URLs.  
- **Avoid dashes** → Slate search treats them as word breaks.  
- **Preferred:**  
EMAIL_UG_COB_Yield_01_Welcome_20250805

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
- `GR_COM` = Graduate – College of Medicine  
- `GR_CPHS` = Graduate – College of Pharmacy & Health Sciences  
- `UG_COB`  = Undergraduate – College of Business  

---
## 1.4 Use Dates for Sorting and Version Control
- Append **YYYYMMDD** to items that repeat or are time‑sensitive.  
- Ensures **chronological sorting** in Slate’s flat folder structure.  
- Example:  
GR_COM_CampusTour_20250926
EMAIL_UG_COB_Yield_01_Welcome_20250805

---
## 1.5 Use Two-Digit Sequence Numbers for Multi-Step Processes
- For campaigns or series of steps, use **01, 02, 03** to keep items in order.  
- Example:  
EMAIL_GR_COM_Interview_01_Invite_20250930
EMAIL_GR_COM_Interview_02_Reminder_20251005

---
## 1.6 Archiving & Cleanup
- Prefix retired items or folders with `Z_` or move to a `Z_Archive` folder.  
- Optionally create **annual archive folders** to manage volume.  
- Examples:  
Z_Archive_2024
Z_UG_COB_Yield_2023

---
## 1.7 Intentional Prefixing to Communicate Risk
- **High‑risk items** (operational queries, live mailing lists) must have **prefixes** to prevent accidental edits.  
- **Low‑risk items** (ad hoc queries, testing) can have simple prefixes like `QRY_` or `TEST_`.

**Training Shortcut:**  
- ✅ Safe to edit: `QRY_`, `TEST_`  
- ⚠ Ask first: `LIST_`, `COM_`, `WFL_`, `POP_`, `EMAIL_`

---
**Next Sections:**  
- Module-Specific Naming Rules for  
1. **Queries**  
2. **Deliver/Email**  
3. **Events**  
4. **Forms**  
5. **Portals**  
6. **Organizations**  
