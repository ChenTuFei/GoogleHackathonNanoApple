Customer Churn Definition Document - BizGrow Q3 Churn Crisis

Context: Q3 churn rate spiked from 4% to 12%, need to identify single biggest churn driver

EXECUTIVE SUMMARY


CHURN DEFINITION FOR THIS CRISIS:
---------------------------------
Primary Definition: Customers whose contracts ended in Q3 2024 (July-September) 
                    and did not renew (renewed_flag = 0)

Formula:
  Q3 Churn Rate = (Q3 contract ended + not renewed) / Total Customers x 100%

Why This Definition:
  1. Directly focuses on the Q3 crisis period (matches problem statement)
  2. Quantifies the specific Q3 churn spike (4% to 12%)
  3. Enables time-based analysis to identify what changed in Q3
  4. Contract data is complete (not affected by EU September log corruption)

What We Are Solving:
  - Identify the single biggest driver of Q3 churn spike
  - Provide actionable recommendation to reduce churn
  - Focus on 80/20 principle (which segment drives the crisis)

What We Are NOT Solving:
  - Historical churn (pre-Q3)
  - Future churn prediction
  - All possible churn causes (focus on 80/20)
  - Product feature improvements (unless it's the main driver)


============================================================
I. CHURN DEFINITION METHODOLOGY EVALUATION
============================================================

For this Q3 churn crisis, we evaluated multiple churn definition approaches:


Method 1: Based on is_churned Field (Standard Definition)
------------------------------------------------------------
Definition: Use the 'is_churned' field from Dataset1
  - is_churned = 1: Customer has churned
  - is_churned = 0: Customer has not churned

Advantages:
  - Simple and direct, already marked in data
  - Covers all historical churned customers
  - Easy to compare with historical data

Disadvantages:
  - Does not distinguish churn timing (cannot focus on Q3 crisis)
  - May include historical churn, diluting Q3 problem severity

Churned Customers: 364 (12.13%)


Method 2: Q3 Contract Ended + Not Renewed (Time-Window Definition)
------------------------------------------------------------
Definition: 
  - contract_end_date in Q3 2024 (2024-07-01 to 2024-09-30)
  - renewed_flag = 0 (not renewed)

Advantages:
  - Directly focuses on Q3 crisis period
  - Directly reflects Q3 churn situation
  - Matches "Q3 churn rate 12%" problem description

Disadvantages:
  - May miss customers who churned before Q3 but affect Q3 data
  - Need to handle EU September data corruption issue

Use Case: Analyzing direct causes of Q3 churn crisis


Method 3: Q3 Contract Ended + Marked as Churned (Combined Definition)
------------------------------------------------------------
Definition:
  - contract_end_date in Q3 2024
  - is_churned = 1

Advantages:
  - Combines time window and churn flag
  - Stricter definition, ensures true churn

Disadvantages:
  - May be too strict, missing some churned customers

Use Case: Conservative estimate of Q3 churn situation


Method 4: Based on Usage Behavior Decline (Behavioral Definition)
------------------------------------------------------------
Definition:
  - Q3-Q4 usage dropped > 50% compared to Q1-Q2
  - Or no login for 30 consecutive days

Advantages:
  - Identifies potential churn risk
  - Can provide early warning

Disadvantages:
  - Usage decline does not equal churn (may just be temporary)
  - Need to combine with contract status to confirm

Use Case: Churn early warning and intervention


Method 5: Combined Definition (Contract + Behavior + Tickets)
------------------------------------------------------------
Definition:
  - contract_end_date in Q3 2024
  - renewed_flag = 0
  - Significant Q3 usage decline
  - Or increased Q3 ticket volume

Advantages:
  - Multi-dimensional validation, more accurate
  - Can identify churn patterns

Disadvantages:
  - Complex definition, may be too strict
  - Need to handle EU September data issue

Use Case: Deep analysis of churn causes and patterns


============================================================
II. SELECTED CHURN DEFINITION FOR THIS ANALYSIS
============================================================

For the Q3 churn crisis, we adopt a **layered definition strategy**:


Primary Definition: Method 2 - Q3 Contract Ended + Not Renewed
------------------------------------------------------------
Rationale:
1. Directly focuses on Q3 crisis period (July-September 2024)
2. Matches problem description "Q3 churn rate spiked from 4% to 12%"
3. Can quantify specific Q3 churned customer count
4. Enables time-based analysis of churn trends

Calculation Formula:
  Q3 Churn Rate = (Q3 contract ended + not renewed customers / Total customers) x 100%

Data Limitations:
  - EU September log data is corrupted, but does not affect contract end date data
  - Contract end date data is complete and can be used for this definition


Supporting Definition: Method 1 - Based on is_churned Field
------------------------------------------------------------
Purpose:
1. Validate results from primary definition
2. Analyze historical churn trends (Q3 vs historical)
3. Identify overall churn patterns

Calculation Formula:
  Overall Churn Rate = (is_churned = 1 customers / Total customers) x 100%


============================================================
III. CHURN IDENTIFICATION CRITERIA (Primary Definition)
============================================================

Q3 Churned Customer Characteristics:
  - contract_end_date between 2024-07-01 and 2024-09-30
  - renewed_flag = 0 (not renewed)
  - Contract has officially ended

Exclusions:
  - contract_end_date is null (still under contract)
  - renewed_flag = 1 (renewed, not churn)
  - contract_end_date not in Q3 (historical or future churn)


============================================================
IV. CHURN RATE CALCULATIONS
============================================================

1. Q3 Churn Rate (Primary Metric)
------------------------------------------------------------
  Q3 Churn Rate = Q3 Churned Customers / Total Customers x 100%
  
  Purpose: Quantify severity of Q3 crisis


2. Overall Churn Rate (Reference Metric)
------------------------------------------------------------
  Overall Churn Rate = Total Churned Customers / Total Customers x 100%
  Current Overall Churn Rate: 12.13%
  
  Purpose: Compare Q3 churn with historical churn


3. Churn Rate by Dimension (Diagnostic Metric)
------------------------------------------------------------
  Calculate churn rate by acquisition channel, product tier, sales segment, etc.
  Purpose: Identify 80/20 driver (which segment has highest churn rate)


============================================================
V. WHAT WE ARE SOLVING VS NOT SOLVING
============================================================

What We Are Solving:
  - Root cause of Q3 churn spike (from 4% to 12%)
  - Identify single biggest churn driver
  - Provide actionable recommendation to reduce churn

What We Are NOT Solving:
  - Historical churned customers (pre-Q3)
  - Future churn risk prediction (though can be mentioned)
  - All possible churn causes (focus on 80/20)
  - Product feature improvement suggestions (unless it's the main driver)


============================================================
VI. DATA NOTES AND LIMITATIONS
============================================================

Data Field Descriptions:
  - contract_end_date: Contract end date (null = still under contract)
  - renewed_flag: Renewal flag (1 = renewed, 0 = not renewed)
  - is_churned: Churn flag (1 = churned, 0 = retained)

Data Quality Limitations:
  - Industry field missing: ~28.7% of records missing industry info (marked as Unknown)
  - EU September log data corrupted: 56,010 records (does not affect contract data, but affects usage behavior analysis)
  - Ticket data coverage: Only 80.7% of customers have ticket data

Handling Approach:
  - Industry missing: Marked as "Unknown", analyzed as separate group
  - EU September data: Excluded or interpolated in usage behavior analysis
  - Ticket missing: Filled with 0, indicating no tickets


============================================================
VII. RATIONALE FOR CHURN DEFINITION SELECTION
============================================================

Why choose "Q3 Contract Ended + Not Renewed" as primary definition?

1. Matches Problem Description
   - Problem explicitly states "Q3 churn rate spiked from 4% to 12%"
   - Need to focus on specific Q3 period churn situation

2. Enables Diagnostic Analysis
   - Can analyze by time dimension (Q3 vs Q1-Q2)
   - Can identify specific Q3 churned customer segments
   - Facilitates validation of three teams' hypotheses

3. Data Availability
   - Contract end date data is complete
   - Not affected by EU September log data corruption
   - Renewal flag data is reliable

4. Actionability
   - Clear definition, easy to calculate
   - Can quantify churned customer count
   - Enables dimension-based grouping analysis


============================================================
DOCUMENT END
============================================================
