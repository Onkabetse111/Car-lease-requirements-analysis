# Car-lease-requirements-analysis
Business Analysis and Data Analysis project using Excel and Power BI to analyse car-lease software requirements, identify high-impact requirements, and develop a proposed requirements prioritisation framework.

---

# Car Lease Requirements & Testing Prioritisation Analysis

## Project Overview

This project analyses a car-lease software requirements dataset using Business Analysis and Data Analysis techniques.

The purpose of the project is to understand the requirements, identify important patterns in the data and create a proposed way to prioritise requirements for planning, development and testing.

The project combines:

- Business Analysis
- Data Analysis
- Requirements Analysis
- Requirements Prioritisation
- Process Analysis
- Data Visualisation
- Power BI
- Excel

---

## Business Problem

A software project can have a large number of requirements.

When there are many requirements, it can become difficult to understand:

- Which requirements are more important?
- Which requirements are more complex?
- Which requirements may require more financial resources?
- Which requirements may need additional testing?
- Which requirements should receive more attention during planning?

This project uses requirement priority, complexity, estimated time and estimated cost to analyse the requirements and propose a structured prioritisation approach.

The dataset contains 2,000 requirements.

---

## Project Objective

The main objective was to create a data-driven approach for understanding and prioritising software requirements.

The analysis aimed to:

1. Understand the requirement dataset.
2. Check the quality of the data.
3. Analyse business priority.
4. Analyse complexity.
5. Analyse estimated time.
6. Analyse estimated cost.
7. Identify high-cost requirements.
8. Identify high-impact requirements.
9. Analyse relationships between variables.
10. Create proposed prioritisation rules.
11. Develop business and functional requirements.
12. Create user stories.
13. Create acceptance criteria.
14. Create a Requirements Traceability Matrix.
15. Design an As-Is process.
16. Design a proposed To-Be process.
17. Build an interactive Power BI dashboard.

---

# Dataset

The dataset contains 2,000 requirement records.

Important fields used in the analysis include:

| Field | Description |
|---|---|
| B_Req | Requirement identifier |
| R_Priority | Numerical business requirement priority |
| FP | Function points / test cases associated with the requirement |
| Complexity | Requirement complexity |
| Time | Estimated time |
| Cost | Estimated cost |

The dataset was originally published as a car-lease software testing dataset.

This project does not assume that the dataset represents the current operations of a specific company. The process and business rules developed in this project are proposed based on the available data.

---

# Tools Used

- Microsoft Excel
- Microsoft Power BI
- GitHub
- DAX
- Data cleaning
- Data analysis
- Business Analysis techniques
- Requirements engineering

---

# Data Preparation

The first step was to inspect the dataset and understand the available fields.

The dataset contained 2,000 requirement records.

The main analytical fields did not contain missing values.

Several completely empty columns were removed from the working dataset.

The requirement ID was also checked to make sure that each requirement could be uniquely identified.

---

# Priority Analysis

The `R_Priority` field contains numerical priority values.

The observed range was:

- Minimum: 1
- Maximum: 294

For analytical purposes, I created three priority bands:

| Priority Band | Range |
|---|---:|
| Low | 1–98 |
| Medium | 99–196 |
| High | 197–294 |

These bands were created for this project and are not official business definitions.

## Priority Distribution

| Priority | Requirements | Percentage |
|---|---:|---:|
| Low | 283 | 14% |
| Medium | 1,356 | 68% |
| High | 361 | 18% |
| Total | 2,000 | 100% |

Most requirements fall into the Medium priority band.

---

# Complexity Analysis

The dataset contains three complexity levels:

- 1
- 3
- 5

I compared complexity against estimated time and estimated cost.

## Complexity and Average Cost

| Complexity | Average Cost |
|---|---:|
| 1 | $18.73 |
| 3 | $56.76 |
| 5 | $94.67 |

The results show a strong increase in average estimated cost as complexity increases.

This was one of the most important findings in the project.

---

# Complexity and Average Time

| Complexity | Average Time |
|---|---:|
| 1 | 3.746 |
| 3 | 3.784 |
| 5 | 3.787 |

Estimated time changes very little across the three complexity levels.

This means that complexity has a much stronger relationship with estimated cost than with estimated time in this dataset.

---

# Priority and Cost

The average estimated cost by priority band was:

| Priority | Average Cost |
|---|---:|
| Low | $53.08 |
| Medium | $57.56 |
| High | $59.15 |

High-priority requirements have the highest average estimated cost, but the difference between the priority groups is relatively small.

This suggests that business priority alone may not be enough to understand potential delivery impact.

---

# Priority and Time

Average estimated time was:

| Priority | Average Time |
|---|---:|
| Low | 3.776 |
| Medium | 3.774 |
| High | 3.763 |

The values are very similar.

This suggests that priority does not strongly distinguish estimated time in this dataset.

---

# Correlation Analysis

Correlation was used to understand relationships between the numerical variables.

| Relationship | Correlation |
|---|---:|
| R_Priority vs Complexity | 0.063 |
| R_Priority vs Time | -0.015 |
| R_Priority vs Cost | 0.041 |
| Complexity vs Time | 0.041 |
| Complexity vs Cost | 0.870 |
| Time vs Cost | 0.446 |

## Main Finding

The strongest relationship is between:

**Complexity and Cost**

with a correlation of approximately:

**0.870**

This is a very strong positive relationship.

Time and cost have a moderate positive relationship of approximately:

**0.446**

The relationships between business priority and the other variables are very weak.

Correlation shows association and does not prove causation.

---

# High-Cost Analysis

The 75th percentile of estimated cost was $75.

For this project, I used:

**Cost > $75**

as the analytical definition of a high-cost requirement.

This produced:

**489 high-cost requirements**

or approximately:

**24.45% of all requirements.**

This threshold is an analytical rule created for this case study and is not an official company threshold.

---

# High-Impact Requirements

I created a proposed definition for a high-impact requirement.

A requirement is considered high-impact when it meets all three conditions:

1. High priority
2. Complexity = 5
3. Cost > $75

Using this definition:

**96 requirements** were identified as high-impact.

This represents:

**4.8% of the 2,000 requirements.**

These requirements could receive additional attention during:

- Requirements review
- Planning
- Development
- Testing
- Resource allocation

The definition is a proposed analytical rule and should be validated with stakeholders before being used in a real project.

---

# Proposed Prioritisation Framework

I created a proposed attention framework using:

- Priority
- Complexity
- Cost

The main rule is:

> High Priority + Complexity 5 + Cost above $75 = Critical

Other combinations receive High, Moderate or Normal attention.

The purpose of this framework is to help teams avoid treating every requirement in exactly the same way.

The rules are proposed for this case study and would need stakeholder validation in a real organisation.

---

# Business Analysis Requirements

The project was extended beyond data analysis into a Business Analysis deliverable.

## Functional Requirements

Examples include:

- The system should allow users to capture and maintain requirements.
- The system should assign business priority to each requirement.
- The system should record complexity.
- The system should record estimated time.
- The system should record estimated cost.
- The system should calculate a recommended attention level.
- The system should identify high-impact requirements.
- Users should be able to filter requirements.
- Users should be able to view requirements requiring additional attention.

---

# Non-Functional Requirements

Examples include:

### Performance

The prioritisation result should be generated within an agreed response time.

### Security

Only authorised users should be able to create, modify or delete requirements.

### Reliability

The prioritisation result should remain accurate when requirement information changes.

### Auditability

Changes to priority, complexity and cost should be traceable.

### Data Integrity

Required fields should not contain invalid or incomplete information.

---

# User Stories

Examples:

### US-001

**As a Project Manager, I want to view software requirements and their business priority so that I can understand which requirements are important.**

### US-002

**As a Business Analyst, I want to record requirement complexity so that delivery impact can be assessed.**

### US-003

**As a Project Manager, I want to view estimated cost so that I can identify requirements that may require additional budget attention.**

### US-004

**As a Project Manager, I want requirements to receive an attention level based on priority, complexity and cost so that resources can be planned consistently.**

### US-005

**As a Business Analyst, I want to identify high-impact requirements so that they can receive additional analysis and testing attention.**

### US-006

**As a QA/Test Lead, I want to filter requirements by priority and complexity so that I can support testing planning.**

---

# Acceptance Criteria

Examples include:

### AC-001

When a requirement exists, its business priority should be visible.

### AC-002

When complexity is entered, it should be stored against the requirement.

### AC-003

When estimated cost is available, it should be visible.

### AC-004

When priority, complexity and cost are available, the system should calculate the appropriate attention level according to the approved rules.

### AC-005

When a requirement has High Priority, Complexity 5 and Cost above $75, the requirement should be classified as Critical.

### AC-006

Requirements meeting the high-impact definition should be flagged.

### AC-007

Users should be able to filter requirements by priority and complexity.

### AC-008

The system should provide a summary of requirements requiring additional attention.

---

# Requirements Traceability Matrix

A Requirements Traceability Matrix was created to connect:

**Business Need → Functional Requirement → User Story → Acceptance Criteria**

This helps show that requirements are connected throughout the analysis process.

The RTM also helps identify requirements that do not yet have supporting user stories or acceptance criteria.

---

# As-Is Process

An illustrative current-state process was created:

```text
Business Requirements Identified
            ↓
Requirements Recorded
            ↓
Business Priority Assigned
            ↓
Complexity, Time & Cost Estimated
            ↓
Requirements Reviewed
            ↓
Testing Requirements Identified
            ↓
Development & Testing Planned
            ↓
Requirements Monitored

The As-Is process is an illustrative case-study process because the source dataset does not document an actual organisation's internal workflow.
```

---

# To-Be Process

A proposed future-state process was designed:

```text
Requirements Identified
            ↓
Requirements Captured
            ↓
Business Priority Assigned
            ↓
Complexity + Time + Cost Recorded
            ↓
Prioritisation Rules Applied
            ↓
High-Impact Requirements Identified
            ↓
Requirements Reviewed & Validated
            ↓
Development & Testing Resources Planned
            ↓
Requirements Approved
            ↓
Development & Testing
            ↓
Monitoring & Change Tracking
```
A decision point was also included:

```text
Requires Additional Attention?
        ↙              ↘
      YES               NO
       ↓                 ↓
Additional Review    Standard Planning
       ↓                 ↓
       └──────→ Requirement Approved
                         ↓
                  Development & Testing
                         ↓
                  Monitoring
```

---

# As-Is vs To-Be

| Current State                                         | Proposed Future State                                 |
| ----------------------------------------------------- | ----------------------------------------------------- |
| Requirements are reviewed                             | Requirements are systematically prioritised           |
| Priority is considered                                | Priority, complexity and cost are considered together |
| High-impact requirements may be difficult to identify | High-impact requirements are explicitly flagged       |
| Testing planning follows review                       | Testing effort can use requirement characteristics    |
| Changes may need manual tracking                      | Changes should be traceable                           |
| Large requirement set                                 | Requirements are grouped by attention level           |

---

# Power BI Dashboard
The Power BI dashboard contains four pages.

## Page 1 — Requirements Overview

This page provides an overall view of:

Total requirements
Priority distribution
Complexity distribution
Average cost
Average time
Priority vs average cost
Priority and complexity distribution

Total requirements:

2,000

## Page 2 — Cost & Complexity Analysis

This page focuses on:

High-cost requirements
High-cost percentage
Average cost by complexity
Average time by complexity
Estimated cost distribution
Estimated time vs estimated cost

Key finding:

### Complexity has a strong relationship with estimated cost.

## Page 3 — Requirements Prioritisation

This page focuses on:

High-impact requirements
High-impact percentage
Attention levels
Priority and complexity
High-impact requirement register

Key result:

### 96 requirements were identified as high-impact using the proposed analytical definition.

## Page 4 — Requirement Explorer

This page allows users to filter requirements using:

Priority
Complexity
High Cost
High Impact
Attention Level

This allows users to move from a high-level dashboard into individual requirement records.

---

# Key Findings

The main findings from the analysis were:

### 1. Most requirements are Medium priority

1,356 of the 2,000 requirements fall into the Medium priority band.

### 2. Complexity has a strong relationship with cost

The average cost increases substantially from Complexity 1 to Complexity 5.

### 3. Complexity has little relationship with estimated time

Average estimated time remains almost the same across the three complexity levels.

### 4. Business priority alone does not explain cost or complexity

The correlations between R_Priority and Complexity, Time and Cost are all very weak.

### 5. High-cost requirements are a significant part of the dataset

489 requirements have estimated costs above the project's $75 threshold.

### 6. A smaller group requires additional attention

96 requirements meet the proposed high-impact definition.

---

# Business Recommendations

Based on the analysis, the following recommendations are proposed:

1. Do not use business priority alone when planning requirements.
2. Consider priority, complexity and estimated cost together.
3. Give additional review to high-impact requirements.
4. Consider additional testing attention for high-complexity requirements.
5. Monitor high-cost requirements during planning.
6. Keep requirement changes traceable.
7. Validate prioritisation rules with business stakeholders before implementation.
8. Use a dashboard to give project managers and analysts a clear view of requirements.

--- 

# Limitations

This project has several limitations.

## Dataset limitation

The dataset does not provide complete information about an actual company's internal processes.

Therefore, the As-Is process and proposed business rules are case-study assumptions rather than verified organisational processes.

## Priority limitation

The priority bands were created for this analysis.

They should be validated with stakeholders before being used in a real project.

## Cost limitation

The $75 high-cost threshold was created using the 75th percentile of the dataset.

It is not an official financial threshold.

## High-impact limitation

The high-impact definition is a proposed analytical framework.

It should be reviewed and approved by stakeholders before production use.

## Correlation limitation

Correlation identifies relationships between variables but does not prove causation.

---

# What I learned
Through this project, I developed practical experience in:

Understanding a business problem
- Cleaning data
- Checking data quality
- Exploring datasets
- Creating analytical categories
- Calculating KPIs
- Performing correlation analysis
- Identifying potential high-impact records
- Creating business rules
- Writing functional requirements
- Writing non-functional requirements
- Creating user stories
- Creating acceptance criteria
- Creating a Requirements Traceability Matrix
- Designing As-Is and To-Be processes
- Building Power BI dashboards
- Creating an interactive requirement explorer
- Communicating findings to a business audience

---

# Project Outcome

The final solution combines Business Analysis and Data Analysis.

The project moves from:

Raw Data

↓

Data Cleaning

↓

Analysis

↓

Business Findings

↓

Requirements

↓

User Stories

↓

Acceptance Criteria

↓

Traceability

↓

Process Analysis

↓

Prioritisation Framework

↓

Power BI Dashboard

This demonstrates how data can support Business Analysis and decision-making.

---

# Future Improvements

If more information were available, the project could be extended by adding:

- Actual stakeholder interviews
- Real business process documentation
- Actual testing results
- Defect data
- Requirement change history
- Development effort
- Actual project costs
- Actual delivery dates
- SQL analysis
- Automated data refresh
- A database
- More advanced prioritisation models

---

# Conclusion

This project demonstrates a practical approach to analysing a large software requirements dataset.

The analysis shows that complexity and estimated cost have a strong relationship, while business priority has weak relationships with cost, time and complexity.

A proposed prioritisation framework was therefore developed to consider multiple requirement characteristics instead of relying on priority alone.

The project also demonstrates the Business Analyst process of moving from data and business questions into requirements, user stories, acceptance criteria, process models and a dashboard.

The prioritisation framework is a proposed case-study solution and should be validated with stakeholders before being used in a real organisation.















