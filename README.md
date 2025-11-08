# 🏡 House Market Overview – Power BI + BigQuery Project

[![Power BI](https://img.shields.io/badge/Power%20BI-Data%20Visualization-F2C811?logo=powerbi&logoColor=white)]()
[![Google BigQuery](https://img.shields.io/badge/Google%20BigQuery-Data%20Warehouse-669DF6?logo=googlebigquery&logoColor=white)]()
[![DAX](https://img.shields.io/badge/DAX-Analytics%20Expressions-00A3E0?logo=powerbi&logoColor=white)]()
[![Power Query](https://img.shields.io/badge/Power%20Query-Data%20Cleaning%20%26%20Transformation-217346?logo=powerbi&logoColor=black)]()
[![Dashboard](https://img.shields.io/badge/Dashboard-Interactive%20Visualization-FFB000?logo=tableau&logoColor=white)]()
[![Visualization](https://img.shields.io/badge/Data%20Visualization-Storytelling%20with%20Data-8A2BE2)]()
[![Time Intelligence](https://img.shields.io/badge/Time%20Intelligence-YTD%20%26%20YOY%20Analysis-1F75FE)]()

![tierra-mallorca-rgJ1J8SDEAY-unsplash](https://github.com/user-attachments/assets/ac8f971c-c5c7-4b53-b406-e361ca9393a3)


### 📊 Project Summary
This project analyzes **housing market trends** using **Google BigQuery** for data processing and **Power BI** for dashboard visualization.  
It provides insights into property prices, sales growth, and regional performance across various house types and sales methods.

---

## 🎯 Project Objective
To understand how factors such as **region, sales type, and house characteristics** influence property prices and sales trends, and to demonstrate advanced Power BI and DAX analytical capabilities.

---

## ⚙️ Tools & Technologies
| Tool | Purpose |
|------|----------|
| **Google BigQuery** | Data extraction, cleaning, and querying large datasets |
| **Power BI Desktop** | Data modeling, visualization, and DAX calculations |
| **SQL** | Used in BigQuery for data preprocessing |
| **DAX (Power BI)** | Created custom measures for KPIs and insights |
| **Excel/CSV** | Raw data format before loading into BigQuery |

---

## 🧮 Key DAX Measures Used
| Measure | DAX Formula | Description |
|----------|--------------|-------------|
| **Total Sales** | `SUM(Housing[purchase_price])` | Total purchase value of all property sales |
| **Last 12 Month Sales** | `CALCULATE(SUM(Housing[purchase_price]), DATESINPERIOD(Housing[date], MAX(Housing[date]), -12, MONTH))` | Calculates total sales over the last 12 months |
| **Units Sold (Latest Yr & Qtr)** | `CALCULATE(DISTINCTCOUNT(Housing[house_id]), YEAR(Housing[date]) = YEAR(MAX(Housing[date])) && QUARTER(Housing[date]) = QUARTER(MAX(Housing[date])))` | Counts unique houses sold in the latest year and quarter |
| **Median Sales Price Change** | Calculates current year vs previous year median price change | Shows YoY price fluctuation by region |
| **YOY Sales Growth** | `((CurrYearSales - PreYearSales) / PreYearSales)` | Year-over-year growth by sales type |
| **Offer to SQM Ratio** | `DIVIDE(SUM(Housing[Offer Price]), SUM(Housing[sqm]))` | Offer price per square meter |
| **Total YTD Sales** | `TOTALYTD(SUM(Housing[purchase_price]), Housing[date])` | Year-to-date accumulated sales |
| **Sales by Region** | `CALCULATE(SUM(Housing[purchase_price]), ALLEXCEPT(Housing, Housing[region]))` | Total sales across regions |
| **Offer Price** | `(100 * Housing[purchase_price]) / (100 - Housing[%_change_between_offer_and_purchase])` | Calculates original offer price from discount percentage |

---

## 📊 Power BI Dashboard Highlights
### Dashboard Images :
<img width="1247" height="721" alt="Screenshot 2025-11-06 071631" src="https://github.com/user-attachments/assets/a1d5f9ef-f862-4cc2-9377-ec39213409dd" />
<img width="1248" height="722" alt="Screenshot 2025-11-06 071707" src="https://github.com/user-attachments/assets/1848854e-ded8-480d-a3b3-b5a0ee4f29b3" />
<img width="1250" height="727" alt="Screenshot 2025-11-06 071740" src="https://github.com/user-attachments/assets/6b62324b-ff51-41c4-ac24-ffa3dd24a7ee" />

### Dashboard Sections:
1. **House Market Overview**
   - YOY Sales Growth by Sales Type  
   - Offer Price vs Purchase Price Scatter  
   - Median Price Change by Region  
   - 12-Month Sales & Units Sold KPIs  
2. **Sales Performance**
   - Total Sales by Region  
   - YTD Sales Progress Table  
   - Average SQM Price by Region
   
3. **Key Influencers**
   - AI insights on what drives Purchase Price (e.g., Age, Region)
4. **Comparative Analysis**
   - Offer-to-SQM Ratio by Sales Type  
   - Average Offer vs Purchase Price by House Type

---

## 💡 Insights Discovered
- **Regular sales** have the highest price per SQM (~15K).  
- **Auction sales** have the lowest offer price per SQM (~11K).  
- **Zealand** and **Jutland** regions dominate sales (95B+ total).  
- **YOY Growth:** Auction sales rose by +29%, while Family sales dropped by -75%.  
- **Property Age:** Newer and heritage homes (Age <16 or >80) have higher purchase prices.  

---

---

## 🚀 How to Run This Project
1. Load raw data into **Google BigQuery** and clean using provided SQL scripts.  
2. Export processed data to **Power BI Desktop**.  
3. Recreate DAX measures using the list above.  
4. View the **interactive dashboard** for insights on sales trends, pricing, and regional performance.

---

## 🏁 Key Takeaways
- Combines **BigQuery** data processing and **Power BI** storytelling.  
- Provides a complete analysis pipeline from data cleaning to dashboarding.  
- Enhances understanding of **real-estate market dynamics** and **DAX time intelligence**.

---

## 👨‍💻 Author
**Praveen S**  
📍 Chennai, India  
💼 Aspiring Data Analyst | Skilled in SQL, Power BI, BigQuery, Python  
🔗 [Portfolio Website](https://praveens2912.github.io/My_Portfolio/)  
🔗 [GitHub Profile](https://github.com/Praveens2912)




---

### 🏷️ Repository Tags
`#PowerBI` `#BigQuery` `#DataAnalytics` `#DAX` `#SQL` `#DataVisualization` `#PraveenS`
