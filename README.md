# 🚂 UK Train Rides – Data Analytics & Forecasting System

**Project Team:** Team 4 (CLS_ONL3_DAT2_G5) [1-3]
**Program:** Digital Egypt Pioneers Initiative (DEPI) – Cohort 3, Data Analytics Track [4-7]
**Status:** Final Graduation Project

---

## 📝 1. Project Overview

This project delivers a comprehensive Data Analytics and Forecasting System designed for the UK rail operator [4, 8, 9]. The goal was to transform raw, unstructured railway journey records into a robust, structured analytical model using Power BI, enabling data-driven insights across operational performance, financial health, and future demand [4].

### 1.1 The Context: A Vital Artery [10, 11]

The UK rail network is the **world's oldest railway system**, established in 1825 [10-13]. It is one of **Europe's busiest railways**, serving approximately **3.5 million passengers daily** [10-13].

### 1.2 Data Scope

The analysis was performed on a transactional ticket dataset [14-16] covering:
*   **Total Tickets Analyzed:** 31,653 [14-18]
*   **Routes Covered:** 65 routes [14, 15, 19, 20]
*   **Stations:** 12 Departure Stations and 32 Arrival Stations [14, 15, 19, 20]

### 1.3 Problem Statement [10, 11, 21]

The railway operator lacked a unified analytics model to cohesively understand the critical drivers of performance. This made answering key operational and financial questions regarding delays, ticket demand, and revenue trends difficult and inefficient [10, 11, 21].

## 🎯 2. Project Objectives [5, 9, 22]

The system was engineered to meet four core objectives:

| Area | Objective | Target KPI / Deliverable |
| :--- | :--- | :--- |
| **Data Engineering** | Clean, preprocess, and transform raw, unstructured railway journey data into an analysis-ready format [5, 9, 22]. | Clean Fact Table (`Fact_Railway`) [23] |
| **Data Modeling** | Build a robust and validated **Star Schema** data model, optimized for performance and scalability in Power BI [5, 9, 22, 24, 25]. | Optimized Star Schema [26, 27] |
| **Business Intelligence** | Develop interactive dashboards with key operational and financial metrics [5, 9, 22]. | Punctuality Target: **87%** [9, 22, 28, 29]; Net Revenue: **£703.22K** [9, 17, 18, 22] |
| **Predictive Analytics** | Create forecasting models for future ride demand, revenue, and ticket class sales [5, 9, 22]. | Next Month Trip Forecast (May 2024) [30-33] |

---

## 🛠️ 3. Methodology & Data Pipeline

The project followed a structured methodology, starting with intensive data processing in Power Query [34, 35].

### 3.1 Key Preprocessing Steps (Power Query) [35-38]

1.  **Data Quality:** Removed duplicate/corrupted rows, and standardized all text fields (station names, ticket classes) using functions like `Text.Trim` and `Text.Proper` [35, 36, 39, 40].
2.  **Date/Time Correction:** Merged separate date and time columns [37, 40]. Crucially, applied **Midnight-Crossing Logic** to correct arrival timestamps for journeys where arrival time was earlier than departure time, ensuring accurate duration calculation [35, 37, 38, 41, 42].
3.  **Derived Fields:** Engineered key metrics like `ActualDelayInMinutes` [35, 37, 43], status flags (`IsCancelled`, `WasDelayed`) [35, 37, 44, 45], composite keys (`Ticket_Key`, `RouteKey`) [35, 37, 45, 46], and `FareBucket` for price segmentation [37, 46, 47].

### 3.2 Data Model Architecture (Star Schema) [24, 25, 27, 48, 49]

The model is built around a central fact table and is optimized for both time-series and geospatial analysis:

*   **Fact Table:** `Fact_Railway` (Contains transactional records, prices, and delay metrics) [26, 50].
*   **Dimension Tables:** `Dim_Date`, `Dim_Tickets`, `Dim_Stations`, `Dim_Purchase`, and `Dim_Status` [26, 27].
*   **Geospatial Integration:** Included `UK_Train_Stations_Coord_Saif` to integrate Latitude/Longitude for map-based analysis [23-25, 51, 52].
*   **Performance Layer:** Used a `Daily_Summary` aggregation table to improve the speed of daily-level visuals and forecasting [26, 52, 53].

---

## 💡 4. Key Findings and Insights

The analysis uncovered significant insights into operational inefficiencies and financial drivers [54, 55]:

| Category | Key Metric / Insight | Source |
| :--- | :--- | :--- |
| **Financial Drivers** | **Advance tickets** are the primary revenue driver, contributing **41.75%** (£293.6K) of Net Revenue [56-60]. | [56, 57] |
| **Top Route** | **London Kings Cross $\rightarrow$ York** is the highest-earning route, generating **£179K** Net Revenue [56-59, 61]. | [56, 57] |
| **Operational Health** | Overall Punctuality is **87%** [28, 29, 54, 55]. Average Delay Time is **3.25 minutes** [19, 20, 28, 29, 54, 55]. | [28, 29] |
| **Cancellation Root Cause** | **Signal Failure** is the single largest cause of cancellations (**519 trips**) [28, 29, 62, 63]. | [28, 29] |
| **Financial Risk** | **Technical Issues** and **Staffing** problems are the leading causes of refunds, contributing to the **£38.70K** total refunded amount [62-66]. | [64, 65] |
| **Future Demand** | Forecasting predicts a **clear increase in total rides** and demand for both Standard and First Class tickets in **May 2024** [30-33, 67]. | [30, 31] |

---

## 📂 5. Repository Structure and Files

This repository contains all essential project files, documentation, and media required for execution and review:

| File / Folder | Description | Status |
| :--- | :--- | :--- |
| `UK_Train_Rides_Analysis.pbix` | **Power BI Project File.** Contains the finalized Star Schema model, DAX measures, and all interactive dashboards [68]. | Ready |
| `Video_Presentation.mp4` | **Project Video Presentation.** A narrated walkthrough of the analysis, methodology, and findings [68]. | Ready |
| `Project_Presentation.pptx` | **Final Presentation File.** Slides covering the project context, objectives, methodology, key results, and strategic recommendations [68]. | Ready |
| `Final_Project_Report.pdf` | **Final Documentation.** Comprehensive report detailing requirements, data preparation, DAX metrics, and business insights [68]. | Ready |
| `Preprocessing_Documentation.pdf` | Detailed documentation of all Power Query transformation steps, including the **Midnight-Crossing Logic** and data standardization procedures [34]. | Ready |
| `Data_Modeling_Documentation.pdf` | Detailed documentation of the **Star Schema** architecture, including Fact Table structure, Dimension attributes, and relationships [27, 69]. | Ready |
| `Raw_Data/` | Folder containing the original raw transactional data source (CSV/Excel) [34, 70-72]. | Ready |

---

## 💻 6. Technologies Used [73]

*   **Business Intelligence & Modeling:** Microsoft Power BI [73]
*   **Data Transformation:** Power Query (M Language) [73]
*   **Calculations & Measures:** DAX (Data Analysis Expressions) [73, 74]
*   **Version Control:** GitHub [73]

## 🤝 7. Team and Acknowledgements

This project was a collaborative effort by Team 4 [1-3] for the Digital Egypt Pioneers Initiative (DEPI) [5, 75, 76].

| Team Member | Role / Key Contribution [2, 77-79] |
| :--- | :--- |
| **Mohamed Ibrahim** (Team Leader) | Lead Data Engineer: Data cleaning, Power Query transformations, Star Schema design, and documentation consolidation [2, 77]. |
| **Mona Mamdouh** | Data Analyst: DAX measures creation, KPI development, and validation [2, 77]. |
| **Dina Hassan** | BI Developer: DAX measures, dashboard visuals, and analysis writing [78, 79]. |
| **Mohannad Abdullah** | BI Developer: Advanced charts, measures, and insight generation [2, 78]. |
| **Abdullah Hassan** | Dashboard Designer: Power BI dashboard layout, UI/UX design, and formatting [78, 79]. |
| **Saif Fekry** | Data Acquisition Specialist: Collecting station longitude/latitude data and map integration setup [78, 79]. |

We extend our deepest gratitude to the **Ministry of Communications and Information Technology (MCIT)** and the **Digital Egypt Pioneers Initiative (DEPI)** for this invaluable opportunity [75, 76].

---

## ⚖️ 8. License

This project is open-source and available under the MIT License.
