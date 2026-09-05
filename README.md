# IT Service Desk & Incident Analytics

![Visitors](https://komarev.com/ghpvc/?username=YOUR_GITHUB_USERNAME&repo=it-service-desk-incident-analytics&label=Visitors&color=0e75b6&style=flat)

![Microsoft Excel](https://img.shields.io/badge/Microsoft%20Excel-Analytics-217346?style=flat&logo=microsoftexcel&logoColor=white)
![PivotTables](https://img.shields.io/badge/Excel-PivotTables-217346?style=flat)
![Dashboard](https://img.shields.io/badge/Analytics-Executive%20Dashboard-5B9BD5?style=flat)
![ITSM Analytics](https://img.shields.io/badge/Domain-ITSM%20Analytics-1F4E78?style=flat)

---

## Table of Contents

- [Overview](#overview)
- [Business Problem](#business-problem)
- [Stakeholders](#stakeholders)
- [Dataset Description](#dataset-description)
- [Tools & Technologies Used](#tools--technologies-used)
- [Skills Demonstrated](#skills-demonstrated)
- [Key Metrics / KPIs](#key-metrics--kpis)
- [Project Workflow](#project-workflow)
- [Repository Structure](#repository-structure)
- [Results](#results)
- [Key Insights & Business Recommendations](#key-insights--business-recommendations)
- [Challenges & Solutions](#challenges--solutions)
- [Project Learnings](#project-learnings)

---

## Overview

**IT Service Desk & Incident Analytics** is an end-to-end Microsoft Excel analytics project developed to transform multi-dimensional IT service data into actionable operational and management insights.

The project analyzes **8 datasets** covering users, technicians, tickets, assets, SLA definitions, customer feedback, incidents, and an additional workbook dataset. The analysis combines structured data validation, PivotTables, PivotCharts, derived bands and flags, conditional formatting, cross-dimensional analysis, KPI development, and executive dashboarding.

The solution was designed around key IT service management questions:

- How much service-desk demand is being handled?
- Which categories, departments, locations, and statuses drive workload?
- How effectively are SLA commitments being met?
- Where are escalations, breaches, and reopened tickets concentrated?
- Which assets create the greatest warranty and replacement-cost exposure?
- Which incident causes and services create the greatest operational disruption?
- How many users are affected by major incidents?
- What is the current customer satisfaction and recommendation level?
- Which areas should management prioritize for operational improvement?

### Project Outcome

The final solution provides:

- **7,000** analyzed tickets
- **98.94%** overall SLA compliance
- **74** SLA breaches
- **1,948** Open/Active tickets
- **556** reopened tickets
- **1,500** assets
- **1,153** warranty-risk assets
- **1,200** incidents
- **570** incidents with 361+ minutes of downtime
- **291** open incidents
- **3,000** customer surveys
- **3.78/5** average customer rating
- **75.1%** customer recommendation rate

The final deliverable is an executive-focused Excel dashboard supported by detailed analytical PivotTables and PivotCharts.

---

## Business Problem

IT service organizations generate large volumes of operational data across service requests, incidents, assets, support personnel, SLAs, and customer feedback. Raw operational records alone do not provide management with a clear view of service performance or operational risk.

The business needed a centralized analytical solution capable of answering the following questions:

### Service Desk Performance

- How many tickets are being handled?
- Which ticket categories generate the greatest demand?
- Which departments and locations generate the highest workload?
- How quickly are tickets receiving their first response?
- How quickly are tickets being resolved?
- How many tickets are escalated or reopened?
- How much workload remains active?

### SLA Management

- What is the overall SLA compliance level?
- How many SLA breaches occurred?
- How do SLA records vary by priority and severity?
- Which ticket types and services have more demanding targets?
- How do response and resolution targets vary by SLA level?
- Which SLA target bands and strictness levels contain the most records?

### Asset Management

- How large is the asset portfolio?
- What is the total replacement-cost exposure?
- How many assets are under repair, retired, in use, or in stock?
- How many assets have expired warranties?
- Which departments, locations, and asset types have the greatest warranty risk?
- Which asset age groups represent potential lifecycle exposure?

### Incident Management

- Which incident types occur most frequently?
- What are the dominant root causes?
- Which incidents create the greatest user impact?
- Which services experience the greatest downtime?
- Which root causes contribute to prolonged downtime?
- How many incidents remain open?
- Which responsible teams handle the greatest incident volume?

### Customer Experience

- What is the overall customer rating?
- What proportion of customers would recommend the service?
- How are ratings distributed?
- How does recommendation behavior change across rating bands?
- Where are positive and negative feedback indicators concentrated?

The project converts these questions into measurable KPIs, comparative analysis, and management recommendations.

---

## Stakeholders

The analysis is designed to support multiple IT and management stakeholders:

| Stakeholder | Business Need |
|---|---|
| **IT Service Desk Manager** | Monitor ticket workload, response/resolution performance, active workload, escalations, and reopenings |
| **IT Operations Manager** | Evaluate operational performance, service disruption, workload, and resource requirements |
| **Incident Management Team** | Identify major incident patterns, root causes, downtime, affected users, and recurring risks |
| **Problem Management Team** | Prioritize recurring root causes and preventive actions |
| **IT Asset Management Team** | Monitor asset inventory, replacement-cost exposure, warranty risk, and lifecycle status |
| **SLA / Service Management Team** | Monitor SLA structures, targets, compliance, breaches, and service commitments |
| **IT Support Team Leads** | Understand technician capacity, ticket workload, and operational bottlenecks |
| **Senior Management** | Review high-level KPIs, operational risks, service performance, and improvement priorities |

---

## Dataset Description

The workbook contains **8 datasets**. Seven datasets were explicitly identified and analyzed during the project workflow.

| Dataset | Business Purpose | Main Analytical Areas |
|---|---|---|
| **Users** | Understand the organizational user population | Department, location, employment type, employment status, hire year, tenure |
| **Technicians** | Understand support workforce and capacity | Specialization, location, experience, shift, employment status, tenure |
| **Tickets** | Measure service-desk workload and performance | Volume, status, category, priority, department, location, response, resolution, SLA, escalation, reopening |
| **Assets** | Analyze inventory, lifecycle, warranty, and financial exposure | Asset type, manufacturer, department, status, age, warranty, replacement cost |
| **SLA** | Analyze service-level commitments and targets | Priority, severity, ticket type, category, service, SLA level, target bands, strictness |
| **Feedback** | Measure customer satisfaction and advocacy | Overall rating, rating bands, recommendation, positive/negative feedback |
| **Incidents** | Analyze service disruptions and operational causes | Incident type, root cause, impact, affected service, affected users, downtime, team, status |
| **Eighth Dataset** | Part of the eight-dataset workbook structure | Included in the workbook; name/fields were not established in the documented analysis |

### Important Data Validation Decisions

The project validated the actual field structure before analysis:

- **Experience Level** was correctly treated as a **Technicians** field rather than a Users field.
- The Assets dataset contains **Replacement Cost**, which was used for financial exposure analysis.
- The SLA dataset does **not** contain a Channel field, so no unsupported Channel analysis was created.
- Existing derived fields and analytical bands were reused where available, including:
  - `Tenure_Band`
  - `Response_Target_Band`
  - `Resolution_Target_Band`
  - `SLA_Strictness`
  - `Response_to_Resolution_Gap`
  - `Impact_Band`
  - `Downtime_Band`
  - `Affected_Users_Band`
  - `Critical_Impact_Flag`
  - `Open_Incident_Flag`
  - `Resolved_Incident_Flag`

---

## Tools & Technologies Used

### Microsoft Excel

The complete analytical workflow was developed in Microsoft Excel using:

- Excel Tables
- PivotTables
- PivotCharts
- Conditional Formatting
- Filtering and sorting
- Aggregation
- Average calculations
- Derived bands and flags
- KPI calculations
- Dashboard design
- Executive reporting

### Analytical Techniques

- Descriptive analytics
- Segmentation
- Trend analysis
- Comparative analysis
- Cross-dimensional analysis
- Operational KPI analysis
- Risk identification
- Service performance analysis
- Customer experience analysis
- Management-focused reporting

---

## Skills Demonstrated

### Data Analysis

- Multi-dataset data analysis
- Data and field validation
- Data aggregation
- KPI development
- Segmentation
- Trend analysis
- Cross-tabulation
- Comparative analysis
- Operational risk identification

### IT Service Management Analytics

- Service desk workload analysis
- SLA performance analysis
- Incident management analytics
- Asset lifecycle analysis
- Warranty risk analysis
- Technician capacity analysis
- Customer satisfaction analysis

### Excel Analytics

- PivotTables
- PivotCharts
- Conditional formatting
- Calculated/derived fields
- Filtering and sorting
- Dashboard construction
- Executive KPI reporting

### Business Intelligence & Communication

- Translating business questions into analytical measures
- Identifying operational bottlenecks
- Converting data findings into business recommendations
- Designing management-focused dashboards
- Communicating measurable results to stakeholders

---

## Key Metrics / KPIs

| Area | KPI | Result |
|---|---|---:|
| **Tickets** | Total Tickets | **7,000** |
| **Tickets** | SLA Compliance | **98.94%** |
| **Tickets** | Average First Response | **1.57 hrs** |
| **Tickets** | Average Resolution | **4.96 hrs** |
| **Tickets** | SLA Breaches | **74** |
| **Tickets** | Escalations | **827** |
| **Tickets** | Reopened Tickets | **556** |
| **Tickets** | Open/Active Tickets | **1,948** |
| **Assets** | Total Assets | **1,500** |
| **Assets** | Warranty Risk Assets | **1,153 / 76.9%** |
| **Assets** | Expired Warranty Assets | **1,106** |
| **Assets** | Total Replacement Cost | **11,450,698.61** |
| **Assets** | Assets Under Repair | **391** |
| **Incidents** | Total Incidents | **1,200** |
| **Incidents** | Open Incidents | **291** |
| **Incidents** | Long-Downtime Incidents | **570 / 47.5%** |
| **Incidents** | Incidents Affecting 1,001+ Users | **716 / 59.7%** |
| **Incidents** | Average Affected Users | **1,232.53** |
| **Incidents** | Average Downtime | **5.86 hrs** |
| **SLA** | SLA Records | **600** |
| **SLA** | Average Response Target | **9.27 hrs** |
| **SLA** | Average Resolution Target | **37.56 hrs** |
| **SLA** | Average Escalation Target | **53.24 hrs** |
| **Feedback** | Surveys | **3,000** |
| **Feedback** | Average Rating | **3.78 / 5** |
| **Feedback** | Recommendation Rate | **75.1%** |
| **Feedback** | Positive Feedback Indicators | **1,912** |
| **Feedback** | Negative Feedback Indicators | **487** |

---

## Project Workflow

The project followed an end-to-end business analytics workflow from raw operational data to an executive management dashboard.

### Phase 1 — Business Requirement Analysis

The project began by identifying the business need for visibility across:

- Service desk workload
- SLA performance
- Asset risk
- Incident disruption
- Technician capacity
- Customer satisfaction

The business questions were converted into measurable analytical requirements.

---

### Phase 2 — Dataset and Field Validation

The available datasets were reviewed to understand:

- Dataset purpose
- Available dimensions
- Available measures
- Existing calculated fields
- Existing bands and flags
- Relationships between business concepts

Field ownership was validated before building analysis.

For example:

- Experience Level → Technicians
- Replacement Cost → Assets
- SLA target fields → SLA
- Incident impact/downtime flags → Incidents

This prevented unsupported analysis and ensured that each PivotTable was based on the correct source fields.

---

### Phase 3 — Data Preparation

The source data was reviewed and prepared for analysis.

Existing analytical fields were leveraged rather than unnecessarily recreating them.

Examples included:

- Tenure bands
- SLA target bands
- SLA strictness
- Response-to-resolution gap
- Impact bands
- Downtime bands
- Affected-user bands
- Incident flags

This created a consistent analytical foundation for the PivotTables.

---

### Phase 4 — Users Analysis

The Users dataset was analyzed to understand organizational structure and user distribution.

Analysis included:

- Users by Department
- Users by Location
- Employment Type
- Employment Status
- Hire Year
- Average Tenure by Department

Key results included:

- Engineering: **122 users**
- HR: **117**
- Legal: **104**
- Procurement: **101**
- Customer Service: **100**
- IT: **86**
- Active users: **90%**
- Average overall tenure: **4.61 years**

---

### Phase 5 — Technicians Analysis

The Technicians dataset was analyzed to understand support capacity and workforce distribution.

Analysis included:

- Technicians by Specialization
- Technicians by Location
- Experience Level
- Shift
- Employment Status
- Average Tenure
- Active Technicians by Experience
- Active Technicians by Shift
- Tenure Bands

Key results:

- **501 active technicians**
- Applications: **87**
- Cybersecurity: **83**
- Database: **81**
- Networking: **80**
- Junior: **162**
- Lead: **147**
- Mid-Level: **146**
- Senior: **145**
- Day Shift: **37%**
- Active technicians: **83%**

---

### Phase 6 — Ticket Analysis

The Tickets dataset became the primary service-desk workload layer.

Analysis included:

- Total ticket volume
- Ticket status
- Ticket category
- Ticket priority
- Department performance
- Location workload
- Technician workload
- Response time
- Resolution time
- SLA breaches
- Escalations
- Reopened tickets
- Monthly ticket trend

Key findings:

- **7,000 tickets** analyzed
- **1,401 Hardware tickets**
- **1,289 Network tickets**
- **1,266 Software tickets**
- **1,201 Access tickets**
- **1,948 Open/Active tickets**
- **827 escalations**
- **556 reopened tickets**
- **74 SLA breaches**

The Open/Active KPI was defined as:

> **In Progress + Open + Pending User = 1,948**

---

### Phase 7 — Asset Analysis

The Assets dataset was analyzed to measure inventory, lifecycle, replacement-cost exposure, and warranty risk.

Analysis included:

- Assets by Type
- Assets by Manufacturer
- Assets by Department
- Assets by Status
- Assets by Age
- Assets by Warranty Status
- Replacement Cost
- Average Replacement Cost
- Warranty Risk
- Warranty Risk by Department
- Warranty Risk by Asset Type
- Warranty Risk by Location

Key findings:

- **1,500 assets**
- **11.45M total replacement-cost exposure**
- **1,153 warranty-risk assets**
- **1,106 expired warranty assets**
- **391 assets under repair**
- **404 assets aged 5–7 years**

---

### Phase 8 — SLA Analysis

The SLA dataset was analyzed to understand service commitments and target structures.

Analysis included:

- SLA by Priority
- SLA by Severity
- SLA by Ticket Type
- SLA by Service
- SLA by SLA Level
- Response Target Bands
- Resolution Target Bands
- SLA Strictness
- Response-to-Resolution Gap
- Ticket Type × Priority
- Category × Severity

Key results:

- **600 SLA records**
- Average response target: **9.27 hrs**
- Average resolution target: **37.56 hrs**
- Average escalation target: **53.24 hrs**
- Critical Support: **220 records**
- Standard: **195**
- Premium: **185**

Response target bands:

- ≤2 Hours: **162**
- 3–4 Hours: **146**
- 5–8 Hours: **137**
- 9+ Hours: **155**

Resolution target bands:

- ≤8 Hours: **162**
- 9–24 Hours: **146**
- 25–48 Hours: **137**
- 49+ Hours: **155**

---

### Phase 9 — Customer Feedback Analysis

The Feedback dataset was analyzed to understand satisfaction and customer advocacy.

Analysis included:

- Customer Ratings Distribution
- Rating Bands
- Customer Recommendation
- Positive Feedback
- Negative Feedback
- Rating × Recommendation
- Rating Band × Recommendation
- Rating Band × Feedback

Key results:

- **3,000 surveys**
- **3.78/5 average rating**
- **2,083 high-rating responses**
- **538 neutral responses**
- **379 low-rating responses**
- **2,253 customers would recommend**
- **747 would not recommend**
- **75.1% recommendation rate**

High-rating customers represented the largest segment, with:

- **1,574 Yes recommendations**
- **509 No recommendations**

---

### Phase 10 — Incident Analysis

The Incidents dataset was analyzed to identify operational disruption, causes, impact, and service risk.

Analysis included:

- Incidents by Type
- Incidents by Root Cause
- Incidents by Impact Level
- Incidents by Affected Service
- Incidents by Responsible Team
- Incident Status
- Downtime Bands
- Affected User Bands
- Critical Impact Flag
- Open Incident Flag
- Resolved Incident Flag

Cross-dimensional analysis included:

- Incident Type × Impact Level
- Root Cause × Impact Level
- Root Cause × Downtime Band
- Affected Service × Downtime Band
- Root Cause × Affected Service

Key results:

- **1,200 incidents**
- **291 open incidents**
- **324 critical-impact incidents**
- **570 incidents with 361+ minutes downtime**
- **716 incidents affecting 1,001+ users**
- **1,232.53 average affected users**
- **5.86 hours average downtime**

---

### Phase 11 — Cross-Dimensional Analysis

The project moved beyond single-dimensional reporting by creating analytical matrices.

Examples included:

#### SLA

- Ticket Type × Priority
- Category × Severity

#### Incidents

- Incident Type × Impact
- Root Cause × Impact
- Root Cause × Downtime
- Affected Service × Downtime
- Root Cause × Affected Service

These matrices were used to identify **where operational problems intersect**, rather than simply ranking categories independently.

---

### Phase 12 — PivotCharts and Visualization

Selected analytical PivotTables were converted into PivotCharts to communicate major patterns visually.

Charts included:

- Tickets by Category
- Tickets by Status
- Monthly Ticket Volume Trend
- SLA Compliance by Priority
- Assets by Status
- Incidents by Downtime Band
- Customer Ratings Distribution
- Customer Recommendation
- Average Response & Resolution Time by Priority

---

### Phase 13 — Executive Dashboard Development

The strongest operational measures were consolidated into an executive dashboard.

The dashboard combines:

- KPI cards
- Operational charts
- SLA performance
- Asset status
- Incident downtime
- Customer experience
- Management highlights

The dashboard provides management with a high-level view without requiring them to navigate every analytical PivotTable.

---

### Phase 14 — Management Insights and Recommendations

The final stage translated analytical findings into business-focused recommendations.

The objective was not simply to report numbers, but to answer:

> **What does this result mean for the business, and what should management do next?**

---

### Phase 15 — Documentation

The complete project methodology, dataset scope, analysis, KPIs, findings, recommendations, challenges, and lessons learned were documented for portfolio and professional presentation.

---

## Repository Structure

```text
IT Service Desk & Incident Analytics/
│
├── 01_Raw_Data/
│   └── IT_Service_Desk_Analytics_Raw_Dataset.xlsx
│
├── 02_Working_Analysis/
│   └── IT_Service_Desk_Analytics_Working.xlsx
│
├── 03_Dashboard/
│   └── IT_Service_Desk_Incident_Analytics_Dashboard.pdf
│
├── 04_Documentation/
│   └── IT_Service_Desk_Incident_Analytics_Project_Documentation.pdf
│
└── Results/
    ├── ticket_performance.png
    ├── sla_performance.png
    ├── asset_analysis.png
    ├── incident_analysis.png
    ├── customer_experience.png
    └── executive_dashboard.png
