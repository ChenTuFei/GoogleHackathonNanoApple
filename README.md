
Churn Definition and Basic Statistics Summary
======================================================================

Generated: 2025-12-14 10:14:19


1. CHURN DEFINITION
----------------------------------------------------------------------
Primary Definition: Contract Ended + Not Renewed (renewed_flag=0)
  - Q3 Churned Customers: 550

Supporting Definition: Based on is_churned field
  - Overall Churned Customers (is_churned=1): 364

Note: Q3 churned customers are NOT marked as is_churned=1 in the data


2. OVERALL CHURN RATE
----------------------------------------------------------------------
Total Customers: 3,000
Overall Churn Rate (is_churned=1): 12.13%
Q3 Churn Rate (of total customers): 18.33%
Q3 Churn Rate (of active at start): 19.59%

Calculation Method:
- Overall Churn Rate (is_churned=1): 364 / 3000 = 12.13%
  * Definition: Based on is_churned=1 field (only includes pre-Q3 churned customers)
  
- Q3 Churn Rate (of total customers): 550 / 3000 = 18.33%
  * Definition: Contract ended + not renewed (renewed_flag=0)
  * Denominator: Total customers (3000)
  
- Q3 Churn Rate (of active at start): 550 / 2808 = 19.59%
  * Definition: Contract ended + not renewed (renewed_flag=0)
  * Denominator: Active customers at start of Q3 (2808 = 3000 - 87 Q1 churned - 105 Q2 churned)
  * Recommended: Use this method for quarterly churn rate (more aligned with business logic)

Historical Quarterly Churn Rates:
  Q1 2024: 2.90%
  Q2 2024: 3.60%
  Q1+Q2 Average: 3.25%

Comparison with Readme:
  Readme states: 'from 4% to 12%'
  Actual: from 3.25% to 18.33%
  Note: Actual Q3 churn rate (18.33%) is higher than readme's 12%


3. TIME TREND ANALYSIS
----------------------------------------------------------------------
Quarterly Churn Rates (Churned / Active at Start of Quarter):
  2024Q1: 2.90% (87 churned from 3000 active)
  2024Q2: 3.60% (105 churned from 2913 active)
  2024Q3: 19.59% (550 churned from 2808 active)
  2024Q4: 15.28% (345 churned from 2258 active)
  2025Q1: 16.00% (306 churned from 1913 active)
  2025Q2: 0.44% (7 churned from 1607 active)

Q3 Monthly Breakdown (Churned / Active at Start of Month):
  July: 6.34% (178 churned from 2808 active)
  August: 6.65% (175 churned from 2630 active)
  September: 8.02% (197 churned from 2455 active)


4. KEY FINDINGS
----------------------------------------------------------------------
- Overall churn rate (is_churned=1): 12.13%
- Q3 churn rate (of total): 18.33%
- Q3 churn rate (of active): 19.59%
- Q3 represents 550 churned customers
- Average ACV of Q3 churned: $36,911.88
- Average onboarding score of Q3 churned: 6.19


======================================================================
