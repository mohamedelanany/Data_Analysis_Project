# 🚂 UK Train Rides – Data Analytics & Forecasting System  
**Project Team:** Team 4 (CLS_ONL3_DAT2_G5)  
**Program:** Digital Egypt Pioneers Initiative (DEPI) – Cohort 3, Data Analytics Track  
**Status:** Final Graduation Project  

---

## 📎 Quick Access – Live Demo & Video

### 🎥 **Project Demo Video (Google Drive)**  
👉 https://drive.google.com/file/d/1msQpyfrmb9HnGxhUNEZYz6ns52Rs88uJ/view?usp=sharing

### 📊 **Live Dashboard (Power BI Service)**  
👉 https://app.powerbi.com/view?r=eyJrIjoiYThkOTkwNDMtZmJmMS00YzgyLWJlZjMtNWEyYjliZDZlNjJkIiwidCI6Ijg4ZmIzZGEyLWY4MDUtNDEwNS1iODAwLWJhZmE1ODgwMjdiZCJ9

---

## 📝 1. Project Overview  
This project delivers a comprehensive Data Analytics and Forecasting System designed for the UK rail operator.  
The goal was to transform raw, unstructured railway journey records into a robust, structured analytical model using Power BI, enabling data-driven insights across operational performance, financial health, and future demand.

### 1.1 The Context: A Vital Artery  
The UK rail network is the world's oldest railway system, established in 1825.  
It is one of Europe’s busiest railways, serving approximately **3.5 million passengers daily**.

### 1.2 Data Scope  
The analysis was performed on a transactional ticket dataset covering:

- **Total Tickets Analyzed:** 31,653  
- **Routes Covered:** 65 routes  
- **Stations:** 12 Departure Stations and 32 Arrival Stations  

### 1.3 Problem Statement  
The railway operator lacked a unified analytics model to cohesively understand the critical drivers of performance.  
This made answering key operational and financial questions regarding delays, ticket demand, and revenue trends difficult and inefficient.

---

## 🎯 2. Project Objectives

| Area | Objective | Target KPI / Deliverable |
|------|-----------|--------------------------|
| **Data Engineering** | Clean, preprocess, and transform raw railway journey data into an analysis-ready format. | Clean Fact Table (Fact_Railway) |
| **Data Modeling** | Build a validated Star Schema model optimized for performance and scalability. | Optimized Star Schema |
| **Business Intelligence** | Develop interactive dashboards with key operational & financial metrics. | Punctuality: 87%, Net Revenue: £703.22K |
| **Predictive Analytics** | Create forecasting models for rides, revenue, and ticket class demand. | Next Month Forecast (May 2024) |

---

## 🛠️ 3. Methodology & Data Pipeline  

### 3.1 Preprocessing Steps (Power Query)  
- Removed duplicates and standardized all text fields (station names, ticket classes).  
- Merged date & time fields and applied **Midnight-Crossing Logic** for accurate duration.  
- Engineered fields such as `ActualDelayInMinutes`, `RouteKey`, `FareBucket`, and status flags.

### 3.2 Data Model (Star Schema)  
- **Fact Table:** Fact_Railway  
- **Dimensions:** Dim_Date, Dim_Tickets, Dim_Stations, Dim_Purchase, Dim_Status  
- Integrated geospatial latitude/longitude for map-based visuals.  
- Added an aggregation table `Daily_Summary` to enhance dashboard performance.

---

## 💡 4. Key Findings & Insights

| Category | Key Insight |
|---------|--------------|
| **Financial Drivers** | Advance tickets contribute **41.75% (£293.6K)** of Net Revenue. |
| **Top Route** | *London Kings Cross → York* generates **£179K**, the highest of all routes. |
| **Operational Health** | Overall punctuality is **87%**, with an average delay of **3.25 minutes**. |
| **Cancellation Cause** | **Signal Failure** is the largest cause of cancellations (519 trips). |
| **Refund Risks** | Technical Issues & Staffing Problems drive most refunds (**£38.70K** total). |
| **Forecasting** | Models predict growth in total rides & ticket demand in **May 2024**. |

---

## 📂 5. Repository Structure & Files  

| File / Folder | Description |
|----------------|-------------|
| **UK_Train_Rides_Analysis.pbix** | Final Power BI file with Star Schema, dashboards, and DAX. |
| **Video_Presentation.mp4** | Project walkthrough (available through the Google Drive link above). |
| **Project_Presentation.pptx** | Final presentation slides. |
| **Final_Project_Report.pdf** | Full project report: requirements, analysis, insights. |
| **Preprocessing_Documentation.pdf** | Documentation for all Power Query transformations. |
| **Data_Modeling_Documentation.pdf** | Explanation of all Star Schema tables & relationships. |
| **Raw_Data/** | Original raw transactional data. |

---

## 💻 6. Technologies Used  
- **Microsoft Power BI**  
- **Power Query (M Language)**  
- **DAX (Data Analysis Expressions)**  
- **GitHub**  

---

## 🤝 7. Team & Acknowledgements  

| Team Member | Role |
|-------------|-------|
| **Mohamed Ibrahim (Team Leader)** | Data Engineering, Power Query transformations, Star Schema design. |
| **Mona Mamdouh** | DAX measures, KPI development, validation. |
| **Dina Hassan** | Dashboard visuals, analysis writing, DAX development. |
| **Mohannad Abdullah** | Advanced visuals, measures, insight generation. |
| **Abdullah Hassan** | Dashboard UI/UX design. |
| **Saif Fekry** | Data acquisition, geographic mapping integration. |

We thank the **Ministry of Communications and Information Technology (MCIT)** and the **Digital Egypt Pioneers Initiative (DEPI)** for their ongoing support.

---

## ⚖️ 8. License  
This project is open-source and available under the **MIT License**.

