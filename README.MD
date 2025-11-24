# 🚚 Amazon Logistics Delivery Performance Analysis  
*End-to-End Excel Data Analytics Project*

<p align="left">
  <img src="https://img.shields.io/badge/Microsoft%20Excel-Data%20Analytics-green?style=for-the-badge&logo=microsoftexcel" />
  <img src="https://img.shields.io/badge/Dashboard-Interactive-blue?style=for-the-badge&logo=tableau" />
  <img src="https://img.shields.io/badge/Statistical%20Analysis-ToolPak-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Pivot%20Tables-Visualization-yellow?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Kaggle%20Dataset-Real%20World-blue?style=for-the-badge&logo=kaggle" />
</p>

---

## 📌 Project Overview
This project analyzes **Amazon delivery performance** using a real Kaggle dataset.  
The objective is to understand how **traffic, weather, distance, time and agent factors** impact delivery efficiency.

A complete **analytics workflow** was executed in Microsoft Excel including:
- Data Cleaning  
- Feature Engineering  
- Descriptive Statistics  
- Correlation Analysis  
- Pivot Tables & Charts  
- Interactive Dashboard & KPIs  
- Actionable Insights + Recommendations  

This project showcases real industry-like problem solving using Excel.

---

## 🎯 Problem Statement
Amazon handles millions of daily deliveries. Even small inefficiencies can result in **high operational cost and delays**.  
This project investigates:

> *What factors contribute most to delay in last-mile delivery?*

---

## 🥅 Project Objectives / Business Questions
1. How do **traffic** & **weather** affect delivery time?  
2. Do different **areas** or **vehicle types** face longer delays?  
3. Does **agent age or rating** influence performance?  
4. At what time of day is **wait time** maximum?  
5. Does **distance** strongly correlate with delivery time?  
6. Which **product categories** are delivered most?

---

## 📂 Files Included in This Repository
<pre>
📁 Amazon-Logistics-Excel-Project
│
├─ 📄 raw_amazon_dataset.csv
├─ 📊 amazon_dataset.xlsx
│ ├─ raw_data
│ ├─ cleaned_data
│ ├─ correlation
│ ├─ descriptive_stats
│ ├─ dashboard 1
│ ├─ dashboard 2
│ ├─ pivot - orders by day
│ ├─ pivot - avg wait time
│ ├─ pivot - avg rating by age
│ ├─ pivot - weather & traffic
│ ├─ pivot - delivery time by area
│ ├─ pivot - category distribution
│ ├─ pivot - orders over time
│
├─ 📷 /images (screenshots folder)
│ ├─ dashboard1.png
│ ├─ dashboard2.png
│
└─ 📘 Project_Report.pdf</pre>
---

## 🧹 Data Cleaning Summary

| Step | Action Performed |
|------|-----------------|
| 1 | Converted dataset into Excel Table (Ctrl + T) |
| 2 | Corrected data types (dates, numeric fields) |
| 3 | Removed duplicates & invalid entries using Sorting & FIltering |
| 4 | Replaced missing values by highlighting using Conditional Formatting & filling with `AVERAGE()` |
| 5 | Standardized formatting for consistency |

---

## 🔧 Feature Engineering

New calculated columns include:

| Column Name | Formula Used | Purpose |
|------------|--------------|---------|
| Day_Name | `=TEXT([@[Order_Date]],"dddd")` | Analyze weekday trends |
| Wait_Time_Min | `=IF([@[Pickup]]<[@Order],(([@Pickup]+1)-[@Order])*1440, ([@Pickup]-[@Order])*1440)` | Time gap before pickup |
| Order_Hour | `=HOUR([@[Order_Time]])` | Assist time-based grouping |
| Hour_Bucket | `=IF([@[Order_Hour]]<8, "Early Morning", IF([@[Order_Hour]]<12, "Morning", IF([@[Order_Hour]]<16, "Afternoon", IF([@[Order_Hour]]<20, "Evening", "Night"))))` | Peak order window mapping |
| Agent_Age_Bucket | `=IF([@[Agent_Age]]<25,"<25",IF([@[Agent_Age]]<=35,"25-35",IF([@[Agent_Age]]<=50,"36-50","50+")))` | Performance segmentation |
| Distance_Km | Haversine formula | Geo-distance vs. delivery time |

---

## 📊 KPIs Tracked on Dashboard
| KPI | Insight Purpose |
|-----|----------------|
| Average Delivery Time | Efficiency measurement |
| Average Wait Time | Pickup delay analysis |
| Average Distance | Route lengths |
| Average Agent Rating | Service quality |
| Total Orders Delivered | Operational volume |

---

## 📈 Visualizations Included

Pivot charts created for:  
1. Orders by Day  
2. Average Wait Time vs Time of Day  
3. Agent Rating by Age Group  
4. Delivery Time vs Traffic & Weather  
5. Delivery Time by Area  
6. Category Wise Distribution  
7. Orders Over Time  

---

## 📸 Project Dashboards
The dashboards are fully interactive and allow filtering by:  
**Traffic • Weather • Area • Category • Vehicle**<br>
![Dashboard 1](images/dashboard1.png)<br>
![Dashboard 2](images/dashboard2.png)

---

## 🧠 Key Insights

- Delivery time **increases by about 60%** during **jammed traffic**  
- Foggy & cloudy weather → **slower deliveries**  
- Night & early morning → **highest wait times**  
- Semi-Urban zones → **highest delays & variability**  
- Distance and delivery time → **positive correlation**  
- Age 25–35 agents → **most consistent performance**  
- Electronics → **highest order demand (~7%)**

---

## 💡 Recommendations
- Route optimization during peak traffic hours  
- Weather-aware delivery scheduling  
- Increase workforce in early morning & night shifts  
- Performance-based route assignment for agents  
- Focus operations more efficiently in semi-urban regions  

---

## 🔮 Future Scope
1. Extend analytics using **Power BI / Python**  
2. Apply **Machine Learning** to predict delivery delays  
3. Expand dataset for more accurate operational mapping  
4. Automate dashboards with real-time data flows  

---

## 🛠 Tech Stack
| Tool | Purpose |
|------|---------|
| Microsoft Excel | Data cleaning & dashboard |
| Haversine Formula | Distance calculation |
| Data Analysis ToolPak | Statistics & correlation |

---

Developed by: **Harshdeep Singh**  
GitHub: [github.com/harshbrar03](https://github.com/harshbrar03)

---

## ⭐ Show Your Support!
If you found this project helpful, please ⭐ **star this repository** to show your support!