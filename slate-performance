# What Slows Slate Down — Performance Impact Guide

This list is ordered from **highest impact → lowest impact** so teams can troubleshoot efficiently and fix root causes before building new datasets or system components.

---

## Highest Impact (Most Likely to Slow Slate)

### 1. Large, Unoptimized Queries  
**Biggest culprit**

Slows when:
- many joins  
- no filters  
- large populations  
- wildcard searches  
- calculated fields inside query  

Explanation:  
It’s like asking a librarian for every book in the building instead of a specific shelf.

---

### 2. Queries Used Inside Portals or Dashboards  
Because they run repeatedly for each user session.

Slows when:
- portal loads trigger live queries  
- dataset not used  
- calculated columns present  

**Rule:**  
If it loads on screen automatically → optimize it.

---

### 3. Rules That Run on Record Save  

Especially rules that:
- look up other records  
- update multiple tables  
- trigger other rules  

**Why:**  
They fire silently and repeatedly.

**Explain it like this:**  
Every save becomes a domino chain.

---

## Medium Impact

### 4. Materialized Views Built Incorrectly  
These should improve speed but slow things if:
- refresh schedules too frequent  
- not filtered  
- used for multiple purposes  

---

### 5. Excessive Real-Time Calculations  

Examples:
- COUNT()  
- MAX()  
- dynamic rankings  
- conditional logic  

Better approach:  
Precompute once in dataset or field instead of calculating every time.

---

### 6. Too Many Concurrent Automations  

Simultaneous processes:
- imports  
- exports  
- communications  
- rule-triggered processes  

Note:  
Slate queues processes, so concurrency matters.

---

## Lower Impact (But Adds Up Over Time)

### 7. Overly Complex Forms  

Too many:
- conditional sections  
- lookups  
- validation rules  

Impact:  
Usually affects user experience more than system performance.

---

### 8. Excessive Permission Layers  

Many nested permissions or realms can slow access checks slightly, especially in portals.

---

### 9. Bad Data Structure Design  

Not immediate slowdown, but causes:
- inefficient queries  
- duplication  
- unnecessary joins  

This is a **long-term performance tax.**

---

## Key Principle

> When Slate feels slow, the cause is almost always system load or design — not the platform itself.

Always diagnose before building.
