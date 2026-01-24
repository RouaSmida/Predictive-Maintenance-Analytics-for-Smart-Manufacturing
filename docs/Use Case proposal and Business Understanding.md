# Predictive Maintenance Analytics for Smart Manufacturing
## Use Case Proposal & Business Understanding

---

## 1. Industry & Organization Context

**Industry:** Industrial Manufacturing / CNC Milling Operations

**Organization (Fictional Scenario):** A medium-sized smart factory operating multiple sensor-equipped CNC milling machines producing three product variants (L, M, H). Machines log operational parameters (air temperature, process temperature, rotational speed, torque, tool wear) during production cycles, generating timestamped event data.

---

## 2. Business Problem Statement

The organization currently faces:

- **Frequent unplanned machine failures** causing production downtime and delayed customer orders
- **Reactive maintenance approach** — interventions occur after failures rather than proactively
- **Limited visibility** into which machines, product types, or operating conditions correlate with failures
- **Absence of data-driven decision support** — maintenance planning relies on fixed schedules or experience rather than predictive analytics
- **High emergency repair costs** — reactive maintenance is significantly more expensive than planned interventions

**Root cause:** Machine sensor data exists but remains fragmented and unanalyzed, with no centralized BI platform to transform raw logs into actionable maintenance intelligence.

---

## 3. Proposed Solution Objectives

This BI project aims to:

1. **Establish machine reliability monitoring** through standardized KPIs tracking failure rates, downtime, and maintenance intervals
2. **Identify high-risk operational patterns** by analyzing correlations between product types, machines, and operating conditions with failure events
3. **Enable predictive maintenance strategies** by developing dashboards that shift maintenance from reactive to proactive
4. **Support resource allocation decisions** with objective data on which assets require priority attention
5. **Define safe operating boundaries** by identifying temperature and tool-wear thresholds associated with increased failure risk

---

## 4. Analytical Questions to Address

The proposed BI solution will investigate **ten key questions**:

1. What is the overall machine failure rate, and how does it distribute across failure modes (HDF, OSF, PWF, TWF, RNF)?
2. Which product types (L, M, H) exhibit higher failure rates during production?
3. Which machines or production lines experience more frequent failures?
4. Under which operating conditions (temperature, torque, speed, tool wear) do failures tend to occur?
5. How do temperature and tool wear levels compare between failed and non-failed operations?
6. How does the failure rate trend over time (daily, monthly, by shift)?
7. Are there identifiable temperature or tool-wear thresholds where failure probability increases?
8. How do failures distribute across different shifts or working days versus weekends?
9. Which product-machine combinations represent the highest risk?
10. What production impact do failures cause, and which preventive interventions would be most effective?

---

## 5. Proposed Key Performance Indicators

The BI solution will implement **eight core KPIs**:

| KPI | Definition | Expected Business Value |
|-----|-----------|-------------------------|
| **1. Machine Failure Rate (%)** | Percentage of production events resulting in failure | Primary reliability metric for system health monitoring |
| **2. Failure Distribution by Mode** | Breakdown of failures by type (HDF/OSF/PWF/TWF/RNF) | Prioritizes root-cause investigation efforts |
| **3. Failure Rate by Product Type** | Failure percentage for each product variant | Identifies products requiring process adjustments |
| **4. Failure Rate by Machine** | Failure percentage per machine or line | Highlights assets needing maintenance priority |
| **5. Temperature Analysis** | Temperature comparison: failed vs normal operations | Establishes thermal thresholds for alerts |
| **6. Tool Wear Analysis** | Tool wear comparison: failed vs normal operations | Defines optimal replacement intervals |
| **7. Temporal Failure Patterns** | Failure trends by time period (shift, day, month) | Reveals scheduling or operational patterns |
| **8. Production Impact Metric** | Percentage of production capacity lost to failures | Quantifies business case for preventive maintenance |

---

## 6. Data Source & Project Scope

**Planned Data Source:** AI4I 2020 Predictive Maintenance Dataset (UCI Machine Learning Repository / Kaggle)

**Dataset Characteristics:**
- 10,000 machine-event records from CNC milling operations
- Features include product type, air/process temperature, rotational speed, torque, tool wear
- Binary failure indicators for overall failure and specific failure modes

**Project Scope:** Analysis will focus on identifying patterns, building predictive models, and creating interactive dashboards to support maintenance decision-making.

---

## 7. Expected Deliverables

The project will produce:

- **Data Model:** Star schema design with fact table (machine events) and dimension tables (Date, Machine, ProductType)
- **ETL Pipeline:** Data cleaning, transformation, and loading scripts
- **Interactive Dashboards:** 
  - Executive Summary view (high-level KPIs)
  - Deep Dive analysis (detailed patterns and correlations)
  - Additional analytical views (forecasts, drill-throughs)
- **Calculated Measures:** DAX formulas for SUM, AVG, YOY, MOM analytics
- **Insights Report:** Findings, recommendations, and implementation roadmap

---

## 8. Expected Outcomes & Benefits

Successful implementation is expected to enable:

✅ **25-35% reduction in unplanned downtime** through predictive maintenance strategies

✅ **20-30% decrease in maintenance costs** by shifting from reactive to planned interventions

✅ **Extended equipment lifespan** through operation within safe parameter boundaries

✅ **Improved production scheduling** with data-driven machine health visibility

✅ **Data-driven culture shift** from intuition-based to analytics-based maintenance decisions

---

## 9. Project Timeline

- **Week 1 (Dec 15):** Use case definition and business understanding *(this document)*
- **Week 2 (Dec 22):** Data preparation and ETL development
- **Week 3 (Dec 29):** Data modeling and star schema implementation
- **Week 4 (Jan 5):** Dashboard development and insights reporting

---

**Project Team:**  Roua Smida, Rooya Jelassi, Mohamed Al Aziz Shabou, Mohamed Nidhal El Moulaa  
**Institution:** Tunis Business School  
**Submitted update:** January 4, 2026
