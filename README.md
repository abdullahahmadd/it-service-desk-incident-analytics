# IT Service Desk & Incident Analytics

![Microsoft Excel](https://img.shields.io/badge/Microsoft%20Excel-Analytics-217346?logo=microsoftexcel&logoColor=white)
![PivotTables](https://img.shields.io/badge/Excel-PivotTables-217346)
![Dashboard](https://img.shields.io/badge/Analytics-Executive%20Dashboard-5B9BD5)
![ITSM Analytics](https://img.shields.io/badge/Domain-ITSM%20Analytics-1F4E78)

---

## Table of Contents

- [Overview](#overview)
- [Business Problem](#business-problem)
- [Objectives](#objectives)
- [Stakeholders](#stakeholders)
- [Dataset](#dataset)
- [Tools & Technologies](#tools--technologies)
- [Methodology](#methodology)
- [Key Performance Indicators](#key-performance-indicators)
- [Key Findings](#key-findings)
- [Business Recommendations](#business-recommendations)
- [Repository Structure](#repository-structure)

---

## Overview

IT Service Desk & Incident Analytics is an end-to-end Microsoft Excel analytics project transforming multi-dimensional IT service data into actionable operational and management insight. It analyzes 8 datasets covering users, technicians, tickets, assets, SLA definitions, customer feedback, and incidents, combining structured data validation, PivotTables, PivotCharts, derived bands and flags, conditional formatting, cross-dimensional analysis, KPI development, and executive dashboarding.

The analysis answers core IT service management questions: how much service-desk demand is being handled, how effectively SLA commitments are being met, where escalations and breaches concentrate, which assets carry the greatest warranty/replacement-cost exposure, which incident causes create the most disruption, and what current customer satisfaction and recommendation levels look like.

---

## Business Problem

IT service organizations generate large volumes of operational data across service requests, incidents, assets, support personnel, SLAs, and customer feedback. Raw operational records alone don't give management a clear view of service performance or operational risk. The business needed a centralized analytical solution answering questions across 5 domains:

- **Service Desk Performance:** ticket volume, category/department/location workload, response and resolution speed, escalation and reopening rates, active workload
- **SLA Management:** overall compliance, breach count, variation by priority/severity, target bands and strictness levels
- **Asset Management:** portfolio size, replacement-cost exposure, warranty risk by department/location/type, lifecycle age exposure
- **Incident Management:** frequent incident types, dominant root causes, user impact, service downtime, open incident volume, responsible team load
- **Customer Experience:** overall rating, recommendation rate, rating distribution, positive/negative feedback concentration

---

## Objectives

- Validate the true field ownership across 8 datasets before building any analysis, to prevent unsupported or misattributed metrics
- Build KPI coverage across tickets, assets, SLA, incidents, and customer feedback in a single connected workbook
- Move beyond single-dimensional reporting into cross-dimensional analysis (e.g., root cause x downtime) to find where operational problems intersect
- Consolidate the strongest operational measures into a single executive dashboard requiring no PivotTable navigation

---

## Stakeholders

| Stakeholder | Business Need |
|---|---|
| IT Service Desk Manager | Monitor ticket workload, response/resolution performance, active workload, escalations, reopenings |
| IT Operations Manager | Evaluate operational performance, service disruption, workload, resource requirements |
| Incident Management Team | Identify major incident patterns, root causes, downtime, affected users, recurring risks |
| Problem Management Team | Prioritize recurring root causes and preventive actions |
| IT Asset Management Team | Monitor asset inventory, replacement-cost exposure, warranty risk, lifecycle status |
| SLA / Service Management Team | Monitor SLA structures, targets, compliance, breaches, service commitments |
| IT Support Team Leads | Understand technician capacity, ticket workload, operational bottlenecks |
| Senior Management | Review high-level KPIs, operational risks, service performance, improvement priorities |

---

## Dataset

The workbook contains 8 datasets; 7 were explicitly identified and analyzed in the project workflow.

| Dataset | Business Purpose | Main Analytical Areas |
|---|---|---|
| Users | Organizational user population | Department, location, employment type/status, hire year, tenure |
| Technicians | Support workforce and capacity | Specialization, location, experience, shift, employment status, tenure |
| Tickets | Service-desk workload and performance | Volume, status, category, priority, department, location, response/resolution time, SLA, escalation, reopening |
| Assets | Inventory, lifecycle, warranty, financial exposure | Asset type, manufacturer, department, status, age, warranty, replacement cost |
| SLA | Service-level commitments and targets | Priority, severity, ticket type, category, service, SLA level, target bands, strictness |
| Feedback | Customer satisfaction and advocacy | Overall rating, rating bands, recommendation, positive/negative feedback |
| Incidents | Service disruptions and operational causes | Incident type, root cause, impact, affected service, affected users, downtime, team, status |
| 8th Dataset | Part of the 8-dataset workbook structure | Included in the workbook; not used in the documented analysis |

**Key data validation decisions:** Experience Level was correctly treated as a Technicians field, not a Users field. Replacement Cost lives in Assets and was used for financial exposure analysis. The SLA dataset has no Channel field, so no unsupported Channel analysis was created. Existing derived fields were reused rather than recreated, including Tenure_Band, Response_Target_Band, Resolution_Target_Band, SLA_Strictness, Response_to_Resolution_Gap, Impact_Band, Downtime_Band, Affected_Users_Band, Critical_Impact_Flag, Open_Incident_Flag, and Resolved_Incident_Flag.

---

## Tools & Technologies

| Category | Tools / Techniques |
|---|---|
| Application | Microsoft Excel |
| Core Features | Excel Tables, PivotTables, PivotCharts, Conditional Formatting, derived bands/flags |
| Analytical Techniques | Descriptive analytics, segmentation, trend analysis, cross-dimensional analysis, operational KPI analysis, risk identification |

---

## Methodology

**1. Business Requirement Analysis**
Identified the business need for visibility across service desk workload, SLA performance, asset risk, incident disruption, technician capacity, and customer satisfaction, converting business questions into measurable analytical requirements.

**2. Dataset & Field Validation**
Reviewed all 8 datasets for purpose, dimensions, measures, and existing calculated fields, validating field ownership (e.g., Experience Level → Technicians, Replacement Cost → Assets) before building any PivotTable, to prevent unsupported analysis.

**3. Data Preparation**
Prepared source data for analysis, reusing existing analytical fields (tenure bands, SLA target bands, impact/downtime bands, incident flags) rather than recreating them, establishing a consistent analytical foundation.

**4. Users Analysis**
Analyzed organizational structure and distribution by department, location, employment type/status, hire year, and average tenure.

**5. Technicians Analysis**
Analyzed support capacity and workforce distribution by specialization, location, experience level, shift, employment status, and tenure.

**6. Ticket Analysis**
Built the primary service-desk workload layer - volume, status, category, priority, department/location workload, technician workload, response/resolution time, SLA breaches, escalations, reopened tickets, and monthly trend.

**7. Asset Analysis**
Measured inventory, lifecycle, replacement-cost exposure, and warranty risk by type, manufacturer, department, status, age, and location.

**8. SLA Analysis**
Analyzed service commitments and target structures by priority, severity, ticket type, service, SLA level, target bands, strictness, and the response-to-resolution gap.

**9. Customer Feedback Analysis**
Analyzed satisfaction and advocacy through rating distribution, rating bands, recommendation rate, and positive/negative feedback cross-tabulated against rating.

**10. Incident Analysis**
Analyzed operational disruption by type, root cause, impact level, affected service, responsible team, status, downtime bands, and affected-user bands.

**11. Cross-Dimensional Analysis**
Built analytical matrices (e.g., Root Cause x Downtime Band, Ticket Type x Priority) to find where operational problems intersect, rather than ranking categories independently.

**12. PivotCharts & Visualization**
Converted the strongest PivotTables into PivotCharts covering tickets, SLA compliance, assets, incident downtime, and customer experience.

**13. Executive Dashboard Development**
Consolidated the strongest operational measures into a single dashboard combining KPI cards, operational charts, SLA performance, asset status, incident downtime, and customer experience - giving management a high-level view without navigating individual PivotTables.

**14. Management Insights & Recommendations**
Translated analytical findings into business-focused recommendations, answering not just "what happened" but "what should management do next."

**15. Documentation**
Documented the complete methodology, dataset scope, analysis, KPIs, findings, and recommendations for professional presentation.

---

## Key Performance Indicators

| Area | KPI | Result |
|---|---|---:|
| Tickets | Total Tickets | 7,000 |
| Tickets | SLA Compliance | 98.94% |
| Tickets | Average First Response | 1.57 hrs |
| Tickets | Average Resolution | 4.96 hrs |
| Tickets | SLA Breaches | 74 |
| Tickets | Escalations | 827 |
| Tickets | Reopened Tickets | 556 |
| Tickets | Open/Active Tickets | 1,948 |
| Assets | Total Assets | 1,500 |
| Assets | Warranty Risk Assets | 1,153 (76.9%) |
| Assets | Expired Warranty Assets | 1,106 |
| Assets | Total Replacement Cost | 11,450,698.61 |
| Assets | Assets Under Repair | 391 |
| Incidents | Total Incidents | 1,200 |
| Incidents | Open Incidents | 291 |
| Incidents | Long-Downtime Incidents | 570 (47.5%) |
| Incidents | Incidents Affecting 1,001+ Users | 716 (59.7%) |
| Incidents | Average Affected Users | 1,232.53 |
| Incidents | Average Downtime | 5.86 hrs |
| SLA | SLA Records | 600 |
| SLA | Average Response Target | 9.27 hrs |
| SLA | Average Resolution Target | 37.56 hrs |
| SLA | Average Escalation Target | 53.24 hrs |
| Feedback | Surveys | 3,000 |
| Feedback | Average Rating | 3.78 / 5 |
| Feedback | Recommendation Rate | 75.1% |
| Feedback | Positive Feedback Indicators | 1,912 |
| Feedback | Negative Feedback Indicators | 487 |

---

## Key Findings

- **Ticket workload is concentrated near-evenly across 4 categories** (Hardware 1,401, Network 1,289, Software 1,266, Access 1,201), meaning no single category dominates demand - the operational bottleneck is volume, not category-specific triage.
- **SLA compliance is high (98.94%) despite meaningful active workload (1,948 open/active tickets)**, indicating the SLA structure itself is well-calibrated to current demand, but the open-ticket backlog still represents a standing operational risk if left unaddressed.
- **Warranty risk affects over three-quarters of the asset portfolio (76.9%, 1,153 of 1,500 assets)**, with 1,106 already past warranty expiration - this is a larger financial exposure than the ticket or incident data alone would suggest, and sits alongside an 11.45M total replacement-cost figure.
- **Incidents affecting 1,001+ users account for nearly 60% of all incidents (716 of 1,200)**, meaning most incidents in this dataset are not minor, isolated events but broad-impact disruptions - reinforcing why root-cause x downtime cross-analysis was prioritized over single-dimension incident counts.
- **Customer recommendation rate (75.1%) is meaningfully lower than what the average rating (3.78/5) alone would suggest**, and high-rating respondents still produced 509 "No" recommendations - indicating rating and advocacy are not perfectly correlated, and a rating-only view would understate the customer risk.

---

## Business Recommendations

1. Prioritize backlog reduction for the 1,948 open/active tickets even though overall SLA compliance is strong, since a large standing backlog is a risk independent of the compliance percentage.
2. Treat warranty risk as a budget-planning input, not just an IT tracking metric - with 76.9% of assets warranty-risk-exposed against an 11.45M replacement-cost base, this has direct financial planning implications.
3. Focus incident response capacity on root causes most associated with long-downtime, high-affected-user incidents, using the root-cause x downtime cross-analysis rather than raw incident-type counts.
4. Investigate the gap between average rating (3.78/5) and recommendation rate (75.1%) directly with customers, since satisfaction and advocacy are diverging in this dataset and a purely rating-based view would miss that.

---

## Repository Structure

```
IT Service Desk & Incident Analytics/
├── 01_Raw_Data/
│   └── IT_Service_Desk_Analytics_Raw_Dataset.xlsx
├── 02_Working_Analysis/
│   └── IT_Service_Desk_Analytics_Working.xlsx
├── 03_Dashboard/
│   └── IT_Service_Desk_Incident_Analytics_Dashboard.pdf
├── 04_Documentation/
│   └── IT_Service_Desk_Incident_Analytics_Project_Documentation.pdf
└── Results/
    ├── ticket_performance.png
    ├── sla_performance.png
    ├── asset_analysis.png
    ├── incident_analysis.png
    ├── customer_experience.png
    └── executive_dashboard.png
```

---
