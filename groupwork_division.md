# BizGrow Customer Churn Analysis Project - Work Plan and Division of Labor

## Project Overview

**Objective**: Present to COO in 8 minutes, identify the single biggest churn driver, and provide actionable recommendations

**Deliverable**: 1 executive-level presentation (PPT/Keynote)

**Timeline**: Hackathon (time-constrained, requires efficient collaboration)

---

## Project Work Breakdown

### Phase 1: Data Preparation and Exploration (2-3 hours)

#### 1.1 Data Loading and Cleaning
- [ ] Load 4 datasets (dataset1, dataset2a, dataset2b, dataset3)
- [ ] Data quality checks (missing values, outliers, data formats)
- [ ] Handle industry field missing values (~30%)
- [ ] Handle EU September log data corruption issue
- [ ] Data merging and linking (based on customer_id)

#### 1.2 Churn Definition and Basic Statistics
- [ ] Define churn clearly (based on is_churned in dataset1)
- [ ] Calculate overall churn rate (Q3 vs historical)
- [ ] Churn rate time trend analysis
- [ ] Basic descriptive statistics

### Phase 2: Diagnostic Analysis - 80/20 Principle (3-4 hours)

#### 2.1 Customer Segmentation Churn Analysis
- [ ] Analyze churn rate by acquisition channel (acquisition_channel)
- [ ] Analyze churn rate by product tier (product_tier)
- [ ] Analyze churn rate by sales segment (sales_segment)
- [ ] Analyze churn rate by region (is_eu)
- [ ] Analyze churn rate by company size (company_size_bucket)
- [ ] Analyze churn rate by onboarding score
- [ ] **Identify segment with highest churn rate (80/20)**

#### 2.2 Usage Behavior Analysis
- [ ] Compare usage patterns: churned vs retained customers
- [ ] Q1-Q2 vs Q3-Q4 usage trend analysis
- [ ] Identify usage decline patterns before churn
- [ ] Handle EU September data missing issue
- [ ] Calculate key usage metrics (activity, engagement)

#### 2.3 Support Ticket Analysis
- [ ] Issue category distribution (product_performance/product_usability/sales_expectation/billing_admin)
- [ ] Analyze issue types for churned customers
- [ ] Correlation between ticket frequency and churn
- [ ] Correlation between response time (first_response_hours) and churn
- [ ] Correlation between sentiment and churn

#### 2.4 Hypothesis Validation
- [ ] **Sales Hypothesis**: "Product is slow causing churn" → Check product_performance tickets
- [ ] **Product Hypothesis**: "Low-quality customers" → Check sales_expectation tickets and acquisition channel
- [ ] **Support Hypothesis**: "Slow response" → Check first_response_hours

### Phase 3: Evidence Validation (1-2 hours)

#### 3.1 Cross-Validation
- [ ] Validate usage logs for high-churn segments
- [ ] Validate ticket patterns for high-churn segments
- [ ] Multi-data source consistency check
- [ ] Exclude data noise (outlier handling)

#### 3.2 Causal Analysis
- [ ] Identify churn temporal patterns (usage decline → ticket increase → churn)
- [ ] Validate causal relationships of key drivers
- [ ] Quantify impact magnitude

### Phase 4: Recommendations (1 hour)

#### 4.1 Problem Identification
- [ ] Determine single biggest churn driver
- [ ] Quantify impact (churn rate, customer count, revenue impact)

#### 4.2 Recommendation Development
- [ ] Develop specific, actionable recommendations
- [ ] Assess recommendation feasibility
- [ ] Estimate recommendation impact (expected improvement)

### Phase 5: Presentation Development (2-3 hours)

#### 5.1 Storyline Design
- [ ] Organize into 4 sections: Setup → Diagnosis → Evidence → Recommendation
- [ ] Ensure logical flow and persuasiveness
- [ ] Focus on "So What" rather than technical details

#### 5.2 Visualization Creation
- [ ] Create key charts (churn rate comparison, segmentation analysis, trend charts)
- [ ] Ensure charts are clear and professional
- [ ] Avoid over-technicalization (do not show Python code)

#### 5.3 Presentation Refinement
- [ ] Refine content on each slide
- [ ] Add data source notes
- [ ] Address EU data missing explanation
- [ ] Final review and rehearsal

---

## Detailed Division of Labor (5-Person Team)

### Member 1: Data Engineer + Churn Definition Lead_JasmineChen

**Primary Responsibilities**:
- Data loading, cleaning, merging
- Handle data quality issues (industry missing, EU September data)
- Define churn criteria
- Basic statistical calculations

**Specific Tasks**:
1. Write data loading scripts (Python/Pandas)
2. Data quality report
3. Data merging (based on customer_id)
4. Basic churn rate calculations
5. Provide cleaned datasets to other members

**Deliverables**:
- Cleaned datasets
- Data quality report
- Churn definition document

**Skills Required**: Python, Pandas, Data Processing

---

### Member 2: Customer Segmentation Analysis Expert

**Primary Responsibilities**:
- Multi-dimensional customer segmentation analysis
- Apply 80/20 principle
- Identify high-churn segments

**Specific Tasks**:
1. Analyze churn rate by acquisition channel, product tier, sales segment, etc.
2. Create segmentation comparison charts
3. Identify segment with highest churn rate
4. Quantify churn contribution of each segment

**Deliverables**:
- Segmentation churn analysis report
- Key comparison charts
- 80/20 analysis results

**Skills Required**: Data Analysis, Statistics, Visualization

---

### Member 3: Usage Behavior Analysis Expert

**Primary Responsibilities**:
- Usage log analysis (dataset2a/2b)
- Pre-churn behavior pattern identification
- Usage trend analysis

**Specific Tasks**:
1. Compare usage patterns: churned vs retained customers
2. Q1-Q2 vs Q3-Q4 usage trend analysis
3. Pre-churn usage decline patterns
4. Handle EU September data missing issue
5. Calculate key usage metrics (activity, engagement)

**Deliverables**:
- Usage behavior analysis report
- Usage trend charts
- Churn early warning indicators

**Skills Required**: Time Series Analysis, Behavior Analysis, Data Visualization

---

### Member 4: Support Ticket Analysis Expert

**Primary Responsibilities**:
- Support ticket analysis (dataset3)
- Correlation between issue types and churn
- Hypothesis validation

**Specific Tasks**:
1. Issue category distribution analysis
2. Analyze issue types for churned customers
3. Correlation between ticket frequency, response time and churn
4. Validate three teams' hypotheses (Sales/Product/Support)
5. Correlation between sentiment and churn

**Deliverables**:
- Ticket analysis report
- Hypothesis validation results
- Issue type distribution charts

**Skills Required**: Text Analysis, Hypothesis Testing, Statistical Analysis

---

### Member 5: Project Manager + Presentation Lead

**Primary Responsibilities**:
- Project coordination and progress management
- Evidence integration and validation
- Recommendation development
- Presentation creation

**Specific Tasks**:
1. Coordinate member work, ensure progress
2. Integrate all analysis results
3. Cross-validate analysis results
4. Determine single biggest churn driver
5. Develop actionable recommendations
6. Create executive-level presentation
7. Organize rehearsal and time control

**Deliverables**:
- Project progress tracking
- Comprehensive analysis report
- Final presentation (PPT/Keynote)
- Recommendation document

**Skills Required**: Project Management, Business Analysis, PPT Creation, Communication Skills

---

## Final Deliverables List

1. **Presentation** (PPT/Keynote) - 8-minute version
2. **Data Analysis Scripts** (Python/Jupyter) - Reproducible
3. **Data Quality Report** - Explain handling approach
4. **Analysis Report** (Optional) - Detailed analysis process
5. **Recommendation Document** (Optional) - Detailed recommendation explanation

---

**Good luck with the project! Remember: Focus on 80/20, tell a good story, provide actionable recommendations!**
