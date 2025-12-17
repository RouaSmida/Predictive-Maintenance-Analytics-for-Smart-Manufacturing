# Predictive Maintenance Analytics for Smart Manufacturing

Business intelligence project using the **AI4I 2020 Predictive Maintenance** dataset to analyze machine reliability and support data‑driven maintenance decisions in a smart manufacturing plant.

---

## 1. Project Overview

This project builds a BI solution for a fictional industrial manufacturer operating CNC milling machines equipped with sensors (temperatures, rotational speed, torque, tool wear). The goal is to transform raw machine logs into dashboards and KPIs that help reduce unplanned machine failures and downtime.

Main components:
- Data preparation and ETL into a star schema.
- Calculation of predictive‑maintenance KPIs (failure rate, MTBF, risk clusters).
- Interactive dashboards for operations and maintenance teams.

---

## 2. Business Understanding

### 2.1 Industry & Organization

- **Industry:** Industrial manufacturing / CNC milling. 
- **Organization (fictional):** A medium‑sized smart factory producing multiple product types (L, M, H) on several sensor‑equipped machines.
- Machines continuously log air temperature, process temperature, rotational speed, torque, and tool wear at each production cycle.

### 2.2 Business Problem

The factory suffers from:
- Frequent **unplanned machine failures**, causing downtime, rush repairs, and delayed customer orders.
- Limited visibility on which machines, product types, or operating conditions are most risky.  
- Maintenance that is mostly reactive or calendar‑based instead of data‑driven.

A Business Intelligence solution is needed to centralize machine data, monitor reliability, and support predictive maintenance decisions.

### 2.3 Business Objectives

The BI solution aims to:
- Monitor overall machine reliability and downtime through standardized KPIs.  
- Identify high‑risk combinations of product type, machine, and operating conditions (temperature, torque, wear) associated with failures. 
- Provide dashboards and indicators that help maintenance planners prioritize interventions and define safe operating windows.

---

## 3. Analytical Questions

The project addresses questions such as:
1. What is the overall machine failure rate, and how is it distributed across specific failure modes (HDF, OSF, PWF, TWF, RNF)? 
2. Which product types, machines, and operating conditions show the highest failure rates?  
3. Are there distinct clusters of operating regimes (cool/normal/hot, low vs high wear), and which clusters are most failure‑prone?  
4. How do reliability KPIs (e.g., Mean Time Between Failures) evolve over time and across machines/lines?  
5. Which assets should be prioritized for preventive maintenance to reduce unplanned downtime?

---

## 4. Key Performance Indicators (KPIs)

Core KPIs used in the dashboards include:

- **Machine Failure Rate (%)** – share of events where `machine_failure = 1`.  
- **Failure Rate by Mode** – HDF, OSF, PWF, TWF, RNF.  
- **Failure Rate by Product Type and Machine.**  
- **Mean Time Between Failures (MTBF)** per machine/line.  
- **Average Process Temperature and Tool Wear at Failure vs Normal Operation.**  
- **Share of Time in High‑Risk Operating Clusters** (derived from clustering on temperature, torque, speed, wear).

---

## 5. Data Model (Star Schema)

### 5.1 Fact Table – `Fact_MachineEvents`

- EventID (PK)  
- DateID (FK → `Dim_Date`)  
- MachineID (FK → `Dim_Machine`)  
- ProductTypeID (FK → `Dim_ProductType`)  
- OperatingClusterID (FK → `Dim_OperatingCluster`)  
- AirTemperature  
- ProcessTemperature  
- RotationalSpeed  
- Torque  
- ToolWear  
- MachineFailure  
- TWF, HDF, PWF, OSF, RNF (binary indicators)

### 5.2 Dimension Tables

- **`Dim_Date`** – DateID, Date, Day, Month, Quarter, Year, Shift.  
- **`Dim_Machine`** – MachineID, Line, Location, CriticalityLevel. 
- **`Dim_ProductType`** – ProductTypeID, Type (L/M/H), Description. 
- **`Dim_OperatingCluster`** – ClusterID, ClusterLabel (e.g., Low‑Risk / Medium‑Risk / High‑Risk), typical ranges of temperature and wear (from clustering).

---

## 6. Tools & Tech Stack

- **Data storage / ETL:** SQL, Python (Pandas) or Power Query. 
- **Analytics & Visualization:** Power BI / Tableau (dashboards & KPIs).  
- **Version control & collaboration:** Git, GitHub, GitHub Copilot.

---

## 7. Dataset

- **Source:** AI4I 2020 Predictive Maintenance Dataset (UCI & Kaggle).  
- **Size:** 10,000 machine‑event records from a milling process.  
- **Main features:** product type (L/M/H), air & process temperature, rotational speed, torque, tool wear, and multiple failure labels.

---

## 8. Repository Structure

.
├─ data/
│ ├─ raw/ # Original AI4I dataset
│ └─ processed/ # Star-schema tables, cleaned data
├─ notebooks/ # EDA, feature engineering, clustering
├─ etl/ # SQL/Python scripts for ETL
├─ dashboards/ # Power BI or Tableau files
├─ docs/ # Project report, slides
└─ README.md

text

---

## 9. Team

- Roua Smida  
- Mohamed Al Aziz Shabou 
- Rooya Jelassi 