# Graduate Enrollment Communication & Data Vocabulary Guide  
**Version 1.0**  
**Applies To:** Slate CRM, Salesforce, Marketing Cloud, Forms, Portals, Queries, Reporting

---

## Purpose

This guide establishes standardized terminology for graduate enrollment communications and data fields across systems.

It applies to:

- Slate forms and portals  
- Applicant-facing communications  
- CRM fields and integrations  
- Query naming conventions  
- Reporting standards  
- Training documentation  

The goal is to ensure:

- Conceptual clarity  
- Data integrity  
- Reporting consistency  
- Reduced ambiguity  
- Scalable CRM architecture  

---

# 1. Identity & Biographical Fields

## 1.1 Legal Name

**Field Labels**
- Legal First Name  
- Legal Middle Name  
- Legal Last Name  

**Definition**  
The name appearing on government-issued identification and official transcripts.

**Usage Notes**
- Required for admissions records, transcripts, financial aid, and visa documentation.
- Do not use “Full Name” (ambiguous and non-structured).

---

## 1.2 Preferred Name

**Definition**  
The name the applicant wishes to be called in communications and portal display.

**Clarifier Language**  
“This does not replace your legal name for official records.”

---

## 1.3 Citizenship / Residency Status

**Field Label:** Citizenship / Residency Status  

**Definition**  
The applicant’s legal relationship to the United States for reporting and visa compliance.

**Standard Options**
- U.S. Citizen  
- U.S. Permanent Resident  
- Non-U.S. Citizen (F-1 Visa)  
- Non-U.S. Citizen (Other Visa)  
- Undocumented / DACA (if institutionally supported)

**Do Not Use**
- “International” (not legally precise)

---

# 2. Academic Intent & Program Selection

Graduate terminology must reflect program specificity.

---

## 2.1 Undergraduate Reference Term: Academic Interest

**Definition**  
A broad area of intended study (e.g., English, Biology, Business).

Used in undergraduate admissions because students may:
- Apply undecided  
- Select multiple interests  
- Change majors  

---

## 2.2 Graduate Standard: Program of Interest

**Field Label:** Program of Interest  

**Definition**  
A specific graduate degree or certificate program to which the applicant intends to apply.

**Examples**
- Master of Science in Data Analytics  
- Doctor of Pharmacy (PharmD)  
- MBA – Healthcare Administration  

Graduate applicants select a defined admissions pathway tied to curriculum, faculty, accreditation, and cohort structure.

**Do Not Use**
- Major  
- Academic Interest  
- Area of Study  

---

## 2.3 Degree Type

**Definition**  
A classification layer used for reporting and filtering.

**Examples**
- Master’s Degree  
- Doctoral Degree  
- Professional Degree  
- Graduate Certificate  

This field does not replace Program of Interest.

---

# 3. Enrollment Timing & Entry Terms

Clear timing terminology is critical for workflow routing and capacity planning.

---

## 3.1 Intended Start Term

**Field Label:** Intended Start Term  

**Definition**  
The academic term the applicant plans to begin enrollment if admitted.

**Example Values**
- Fall 2026  
- Spring 2027  
- Summer 2026  

This field drives:
- Admissions workflow routing  
- Cohort planning  
- Capacity modeling  

---

## 3.2 Preferred Start Term (Optional)

Use only when flexibility exists.

**Definition**  
The applicant’s preferred term if multiple entry points are available.

If programs operate in structured cohorts, use **Intended Start Term only**.

---

# 4. Academic Standing & Entry Level

Graduate terminology must not mirror undergraduate classifications.

---

## 4.1 Current Level of Study

**Definition**  
The applicant’s academic status at the time of application.

**Standard Options**
- Senior (Bachelor’s in Progress)  
- Bachelor’s Degree Completed  
- Master’s Degree Completed  
- Currently Enrolled in Graduate Program  
- Professional Degree Completed  

Used to determine:
- Eligibility  
- Transcript requirements  
- Conditional admission logic  

---

## 4.2 Entry Classification (Graduate Context)

Undergraduate categories such as Freshman or Transfer must not be reused.

**Graduate Standard Options**
- First-Time Graduate Student  
- Graduate Transfer Student  
- Non-Degree Seeking  
- Certificate-Only Applicant  

---

# 5. Enrollment Status Definitions

To align reporting across Slate, Salesforce, and Marketing Cloud:

- **Applicant** – Submitted an application  
- **Admitted** – Offered admission  
- **Deposited** – Paid enrollment deposit  
- **Enrolled** – Registered for courses  
- **Matriculated** – Officially began program  

Each status must have a documented trigger event in system governance documentation.

---

# 6. Language Standards for Forms

Forms must reflect precision expected at the graduate level.

**Use**
- “Select your Program of Interest”  
- “Indicate your Intended Start Term”  
- “What is your current level of study?”

**Avoid**
- “What would you like to study?”  
- “When do you want to start?”  
- “Are you in college?”

---

# 7. Slate Field Alignment Recommendations

| Concept | Recommended Field Label | Required | Primary Use |
|----------|------------------------|----------|-------------|
| Program | Program of Interest | Yes | Workflow + Reporting |
| Term | Intended Start Term | Yes | Cohort Planning |
| Degree Type | Degree Level | No | Reporting |
| Academic Background | Current Level of Study | Yes | Eligibility Logic |
| Entry Classification | Entry Type | Yes | Workflow Routing |

---

# 8. Controlled Vocabulary Rules

1. Do not use synonyms across systems.  
2. Do not rename fields without governance review.  
3. All new forms must reference this guide.  
4. Undergraduate and Graduate vocabulary must remain distinct.  
5. Deviations must be documented in the Data Standards repository.  

---

# 9. Governance Statement

Graduate enrollment language must reflect:

- Program specificity  
- Cohort structure  
- Accreditation implications  
- Visa requirements  
- Capacity management  

Language ambiguity creates:

- Reporting distortion  
- Workflow errors  
- Integration failures  
- Poor user experience  

Standardized vocabulary supports scalable CRM architecture and institutional clarity.

---

# Document Control

**Repository:** enrollment-data-standards  
**Maintained By:** Enrollment Systems & Operations  
**Review Cycle:** Annual or upon program structure change  
