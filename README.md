# 🏨 HotelRevAI — AI Driven Revenue Analysis for Hotels
 
> **Infosys Springboard Virtual Internship 6.0** · Batch 13 · Group 2 · Team D  
> Mentor: **Selciya** · Duration: **8 Weeks** · Feb 2026 – Mar 2026
 
---
 
## 📌 Project Overview
 
**HotelRevAI** is an interactive, AI-driven revenue analysis system for the hotel industry built entirely on **Microsoft Power BI**. It transforms **1,17,430 raw hotel booking records** into actionable business intelligence through **5 fully interactive dashboards** — replacing manual Excel reporting with a single, filterable BI system.
 
| Metric | Value |
|---|---|
| 📊 Records Processed | 1,17,430 |
| 📈 Dashboards Built | 5 |
| 🧮 DAX Measures Created | 13 |
| 🗂️ Columns in Final Dataset | 32 |
| 💰 Total Revenue Analyzed | $42.72M |
| 📅 Data Period | 2015 – 2017 |
 
---
 
## 👥 Team Members
 
| # | Name |
|---|---|
| 1 | Chelikani Harshal |
| 2 | Satbir Singh |
| 3 | Arun Kumar |
| 4 | N. Akhila |
| 5 | G. Srilakshmi |
 
---
 
## 🎯 Project Objectives
 
- Load, clean & preprocess **1,17,430 hotel booking records** using Power Query Editor
- Build **13 DAX measures** covering Revenue, ADR, RevPAR, Occupancy %, Cancellation Rate & more
- Design **5 interactive dashboards** covering Revenue, Occupancy, Guests, Cancellations & Strategy
- Empower hotel GMs & Revenue Managers with faster, data-driven decisions
- Replace manual Excel reporting with a single, cross-filterable BI system
 
---
 
## 🛠️ Tech Stack
 
| Technology | Purpose |
|---|---|
| 📊 Microsoft Power BI Desktop | Primary dashboard development & reporting tool |
| 🔧 Power Query Editor | Data cleaning, transformation & preprocessing |
| 📐 DAX (Data Analysis Expressions) | Business metric calculations & KPI measures |
| 💡 M Language | Custom column formulas within Power Query |
| 📁 Microsoft Excel (.xlsx) | Source data format — `hotel_booking_main.xlsx` |
 
---
 
## 📂 Repository Structure
 
```
📦 HotelRevAI
 ┣ 📂 Dataset
 ┃ ┗ 📄 hotel_booking_main.xlsx
 ┣ 📂 Milestone 1
 ┃ ┗ 📄 Harshal Milestone 1 Report.docx
 ┣ 📂 Milestone 2
 ┃ ┗ 📄 Milestone 2 report.docx
 ┣ 📂 Milestone 3
 ┃ ┗ 📄 Harshal Milestone 3 report.docx
 ┣ 📂 Milestone 4
 ┃ ┗ 📄 Harshal Milestone 4 report.docx
 ┣ 📊 HotelRev-Ai Dashboards.pbix
 ┣ 📑 HotelRev-Ai_Final_Presentation.pptx
 ┗ 📝 Internship_Completion_Report.docx
```
 
---
 
## 📊 Dataset Overview
 
- **Raw Records:** 1,19,390
- **Clean Records:** 1,17,430 (after filtering ADR = 0 rows)
- **Columns:** 36 → 32 (after removing 6 irrelevant columns)
- **Data Period:** 2015 – 2017
 
### Data Cleaning Steps
- ✅ Enabled column profiling across all rows
- ✅ Replaced nulls in `country`, `agent` & `company` columns
- ✅ Removed 6 irrelevant / personal data columns
- ✅ Filtered out rows where ADR = 0
- ✅ Corrected data types for all 32 columns
- ✅ Created 4 custom columns via M language
 
### Custom Columns Created (M Language)
 
| Column | Description |
|---|---|
| `total_nights` | Sum of weekend + weekday nights stayed |
| `guest_type` | Couple/Group, Family, or Solo classification |
| `season` | Autumn / Spring / Summer / Winter mapping |
| `revenue` | ADR × total_nights (calculated revenue) |
 
---
 
## 🧮 DAX Measures & KPIs
 
| KPI | Value | Formula |
|---|---|---|
| 💰 Total Revenue | $42.72M | `SUM(revenue)` |
| 📋 Total Bookings | 119.39K | `COUNTROWS()` |
| 🏷️ Avg Daily Rate (ADR) | $101.83 | `AVERAGE(adr)` |
| 📈 RevPAR | 64.11% | Revenue / Capacity |
| 🛏️ Occupancy % | 62.96% | Checked-Out / Total |
| ❌ Cancellation Rate | 37.04% | Cancelled / Total |
| ⏱️ Avg Lead Time | 104 days | `AVERAGE(lead_time)` |
| 🌙 Total Nights Stayed | 409.26K | `SUM(total_nights)` |
| 🔁 Repeat Guest % | 3.19% | Repeat / Total × 100 |
| 🚫 No Show Count | 1.21K | `COUNTROWS(no-show)` |
| 🗑️ Total Cancelled | 44.22K | `COUNTROWS(cancelled)` |
| 💵 Revenue per Booking | $0.36K | Revenue / Bookings |
| ⭐ Avg Special Requests | 0.57 | `AVERAGE(special_req)` |
 
---
 
## 📺 Dashboards Built
 
### Dashboard 1 — Revenue & Booking Performance
> KPI cards · Revenue trend · Channel donut · Market segment bar · Occupancy by month
 
**Key Insights:**
- Total Revenue: $42.72M across 119.39K bookings
- Online TA dominates booking channels at **82% share**
- August records highest revenue; January shows the lowest
- City Hotel drives higher booking volumes overall
 
---
 
### Dashboard 2 — Occupancy & Revenue Analysis
> ADR vs RevPAR trend · Weekend vs Weekday · Revenue by Room Type · ADR by Room Type
 
**Key Insights:**
- Resort Hotel occupancy peaks during **summer months**
- Weekend stays consistently outperform weekday stays
- RevPAR trend follows ADR closely across all months
 
---
 
### Dashboard 3 — Guest Analysis & Segmentation
> Map visual · Guest type donut · Lead time by guest · Top 10 countries · Meal plan donut
 
**Key Insights:**
- Transient guests form the largest booking segment (**74%+**)
- **Portugal (PRT)** is the #1 source country by total bookings
- BB (Bed & Breakfast) is the most popular meal plan at **77%**
 
---
 
### Dashboard 4 — Cancellation & Forecasting Trends
> Cancellation by month · Lead time histogram · Forecast line · Deposit type analysis
 
**Key Insights:**
- Overall cancellation rate: **37.04%** — 44.22K bookings
- City Hotel cancellation rate (**41.73%**) far exceeds Resort Hotel (**27.76%**)
- Short lead-time bookings (0–7 days) show the **lowest cancellations**
 
---
 
### Dashboard 5 — Revenue Strategy & Pricing Insights
> ADR by room & season · Revenue by segment · Country revenue · Meal plan revenue
 
**Key Insights:**
- Room Type H commands the highest ADR across all seasons (**$656**)
- Portugal drives the highest total revenue among all source countries
- BB meal plan accounts for **72.97%** of all meal plan revenue
 
---
 
## 💡 Key Business Insights
 
| # | Insight | Recommendation |
|---|---|---|
| 📈 | **Revenue Seasonality** — August–September peak, January–February weakest | Dynamic pricing in off-peak months |
| 🏨 | **Hotel Type Gap** — City Hotel cancellation (41.73%) vs Resort (27.76%) | Non-refundable deposit policies |
| 🌍 | **Top Source Markets** — Portugal, Great Britain, France | Targeted marketing campaigns |
| 🛏️ | **Room Type Pricing** — Room H commands highest ADR ($656+) | Prioritise premium room availability in peak seasons |
| ⚡ | **Lead Time & Cancellations** — 0–7 day bookings have lowest cancellations | Last-minute deals for high-demand periods |
| 🎯 | **Channel Dominance** — Online TA drives 82% of bookings | Invest in OTA visibility and reviews |
 
---
 
## 🗓️ Project Timeline
 
| Week | Activities |
|---|---|
| Week 1 | Dataset study & domain understanding |
| Week 2 | Power BI setup, data loading & null handling |
| Week 3 | Power Query transformations & custom columns |
| Week 4 | 13 DAX measures & KPI development |
| Week 5 | Dashboards 1 & 2 built and reviewed |
| Week 6 | Dashboards 3 & 4 with map & forecast |
| Week 7 | Dashboard 5 & business insights derived |
| Week 8 | Final documentation & completion report |
 
---
 
## 🏆 Key Milestones
 
| Milestone | Description | Date |
|---|---|---|
| 🚀 Project Kickoff | Orientation, dataset received & studied | 05-02-2026 |
| 📝 Prototype / First Draft | Data loaded, Power Query cleaning done, custom columns created | 11-02-2026 |
| 🔍 Mid-Term Review | All 13 DAX measures created, first 2 dashboards built | 20-02-2026 |
| ✅ Final Submission | All 5 dashboards completed & tested | 13-03-2026 |
| 🎤 Presentation | Project presented to mentor with dashboard walkthrough | 24-03-2026 |
 
---
 
## 🔄 Real-World Impact
 
| Before HotelRevAI | After HotelRevAI |
|---|---|
| ❌ Static Excel Reports | ✅ 5 Interactive Dashboards |
| ❌ Hours of manual data prep | ✅ Instant cross-filtered views |
| ❌ Siloed metric tracking | ✅ All KPIs in one system |
| ❌ Delayed decision making | ✅ Real-time business answers |
| ❌ No forecasting capability | ✅ Booking forecast trend line |
 
---
 
## 🎓 About
 
This project was developed as part of **Infosys Springboard Virtual Internship 6.0** under the mentorship of **Selciya**.  
**Batch 13 · Group 2 · Team D** · Duration: Feb 2026 – Mar 2026
 
---
 
*HotelRevAI — Turning raw booking data into revenue intelligence.*
