
# Hackathon Problem Statement

## Understanding Customer Churn

---

## Business Scenario

You are the **Analytics Task Force** for **BizGrow**, a SaaS platform that helps small and medium-sized businesses manage inventory.

Until recently, BizGrow experienced rapid growth. However, the Q3 results have just been released — and they are alarming:

> **Customer churn has increased from 4% to 12% in a single quarter.**

An emergency meeting has been called by the **Chief Operating Officer (COO)**. Unfortunately, internal teams disagree on the root cause:

* **Sales Leadership** claims:
  *“The product is broken — customers are leaving because the new dashboard is too slow.”*

* **Product Leadership** claims:
  *“Sales is acquiring low-quality customers who go out of business within three months. The product is fine.”*

* **Customer Support** claims:
  *“We are overwhelmed by support tickets, and customer feedback is not being addressed.”*

The COO has asked your team for help — with very clear constraints.

---

## The Executive Request

The COO does **not** want:

* A dashboard
* A list of 50 charts

They want **one thing only**:

> **“We have limited resources. Identify the single biggest leak in customer retention and give me one clear, actionable recommendation to fix it. Convince me this is the right decision.”**

---

## The Data

You are given access to **three raw datasets**, each with real-world data quality issues that must be addressed during analysis.

### 1. Salesforce Export

* Contract start and end dates
* Company size
* Industry
* **Known issue:** ~30% of the industry field is missing

### 2. Usage Logs

* Daily customer login activity
* **Known issue:** European server logs are corrupted for September

### 3. Support Tickets

* Unstructured text data describing customer complaints
* Mix of Sales-related and Product-related issues

---

## The Deliverable

Your team has **8 minutes** to present a **slide deck** to the COO.

The deck must:

* Tell a **coherent story**
* Lead clearly to **one recommendation**
* Be **executive-ready**

Although you submit **one deck**, your narrative must demonstrate that you followed the **Analytics Project Lifecycle** taught in this course.

---

## Required Narrative Structure

### I. The Setup — Problem Definition

* Do **not** simply report “churn.”
* How did your team **define churn** for this specific crisis?
* What is **in scope**, and what is **out of scope**?

---

### II. The Diagnosis — Prioritization

* You cannot fix everything.
* Use the **80/20 principle** to identify:

  * Which customer segment
  * Or which behavioral pattern
    is driving the majority of churn.

---

### III. The Evidence — Validation

* Prove your diagnosis is **real**, not data noise.
* How did you:

  * Handle missing industry data?
  * Address corrupted EU usage logs?
  * Cross-validate insights across multiple datasets?

---

### IV. The Recommendation — Action

* End with a **single, concrete recommendation**.
* It must be:

  * Actionable
  * Realistic
  * Directly tied to your analysis
* The COO should clearly understand:

  > *“If we do this, churn will go down.”*

---

## Evaluation Rubric

| Criteria                         | Weight | What We Are Looking For                                                         |
| -------------------------------- | ------ | ------------------------------------------------------------------------------- |
| **Problem Scoping**              | 25%    | Clear definition of the problem and scope. Logical handling of missing EU data. |
| **Analytical Rigor**             | 25%    | Identification of the true 80/20 churn driver. Validation across data sources.  |
| **Business Logic**               | 25%    | Recommendation makes business sense (e.g., not “fire the sales team”).          |
| **Storytelling & Communication** | 25%    | Executive-ready deck focused on insights and decisions, not code screenshots.   |

---

## Key Reminder

This is **not** a technical exercise.

This is a **decision-making exercise**:

> Use analytics to **reduce ambiguity**, **prioritize action**, and **drive impact**.

