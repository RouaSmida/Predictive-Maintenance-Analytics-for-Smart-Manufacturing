# Predictive Maintenance Analytics for Smart Manufacturing


## 📋 Project Overview

A Business Intelligence solution analyzing predictive maintenance data from CNC milling machines to identify failure patterns, high-risk operating conditions, and actionable recommendations for reducing unplanned downtime.

**Key Findings:**
- 3.39% overall failure rate (339 failures in 10,000 events)
- Machine B exhibits 15% higher failure rate than average
- Heat Dissipation Failure (HDF) is the dominant failure mode (~32%)
- Tool wear beyond 130 minutes correlates with increased failure risk

## 👥 Team Members

| Name | Responsibilities |
|------|------------------|
| Roua Smida | Use Case Proposal, ETL Pipeline, Data Dictionary |
| Rooya Jelassi | Data Modeling, DAX Measures |
| Mohamed Al Aziz Shabou | Insights Report |
| Mohamed Nidhal El Moulaa | Dashboard Development |

## 🔧 Technical Stack

- **ETL:** Python 3.x, Pandas
- **Data Modeling:** Power BI (Star Schema)
- **Visualization:** Power BI Desktop
- **Documentation:** Markdown, LaTeX

## 📊 Data Source

**AI4I 2020 Predictive Maintenance Dataset**  
Source: UCI Machine Learning Repository / Kaggle  
Records: 10,000 machine events  
Features: Temperature, rotational speed, torque, tool wear, failure indicators

## 🚀 How to Use

1. **Run ETL Pipeline:**
   ```
   Open etl/etl_ai4i.ipynb in Jupyter/VS Code
   Run all cells to generate processed CSVs
   ```

2. **Open Dashboard:**
   ```
   Open dashboard/Predictive_Maintenance_BI.pbix in Power BI Desktop
   ```

3. **View Report:**
   ```
   Open report.pdf for insights and recommendations
   ```

## 📈 Key Deliverables

- ✅ Use Case Proposal with 10 analytical questions and 8 KPIs
- ✅ Star Schema data model (1 Fact + 3 Dimensions)
- ✅ ETL Pipeline with documented transformations
- ✅ Interactive Power BI Dashboard (2 pages)
- ✅ 12+ DAX Measures (SUM, AVG, CALCULATE, etc.)
- ✅ Comprehensive Insights Report with 8 recommendations

---

**Institution:** Tunis Business School  
**Course:** IT300 - Business Intelligence  
**Date:** January 2026
