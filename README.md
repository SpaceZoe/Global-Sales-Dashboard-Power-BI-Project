# 🌍 Global Sales Dashboard - Power BI Project

> **An interactive, end-to-end BI solution designed for analyzing global e-commerce performance.**

This project demonstrates a professional approach to **Data Engineering** and **Visualization** within Power BI. Starting from raw Excel data, I engineered a robust **Star Schema** data model and implemented advanced **DAX calculations** to deliver actionable insights on Sales, Units, and Average Selling Price (ASP) across multiple dimensions.

---

## 📸 Dashboard Preview

### 1. 🛒 Executive Sales Dashboard
*A high-level overview for stakeholders, featuring dynamic slicers and KPI cards.*
![Sales Dashboard]
* **Key Features:** Interactive Slicers (Year, Country, Product), KPI Cards with millions/thousands formatting, and cross-filtering visuals.

### 2. 💸 Discount Analysis & Detail Table
*Granular view of product performance, highlighting discount impact on sales.*
![Discount Details]
* **Key Features:** Conditional Formatting on data bars, calculated columns for Discount Rate, and tabular breakdown for deep dives.

### 3. ⏱️ Advanced Time Intelligence
*Complex DAX implementation for trend analysis and period-over-period comparison.*
![Time Intelligence]
* **Key Features:** `TOTALYTD`, `SAMEPERIODLASTYEAR`, and custom `Month Slicer` logic to analyze Sales trends over time.

### 4. 📊 Advanced Tooltips (Contextual Insights)
*Hover-over capabilities to show detailed breakdowns without cluttering the main dashboard.*
![ASP Tooltip]
* **Key Features:** Visual Tooltip showcasing ASP distribution by Product Category.

### 5. ℹ️ Documentation & Definitions
*Built-in documentation page to ensure data governance and user understanding.*
![Info Page]
* **Key Features:** Clear definitions of metrics (ASP, Discount Rate) and data lineage info.

---

## ✨ Key Technical Highlights

This project goes beyond basic visualization by implementing advanced **BI Engineering** practices:

| Feature | Engineering & Technical Implementation |
| :--- | :--- |
| **Data Modeling** | Designed a **Star Schema** with Fact Tables (Sales) and Dimension Tables (Date, Product, Geography) to optimize query performance. |
| **Advanced DAX** | Created complex measures for **Time Intelligence** (YoY%, YTD, MTD) and **Dynamic KPIs** that switch based on user selection. |
| **UX/UI Design** | Implemented **Page Navigation** (Buttons & Bookmarks) and **Visual Layering** to create an app-like user experience. |
| **Performance** | Optimized visual interactions and reduced data model size by removing unnecessary columns and using proper data types. |

---

## 🧠 Business Logic & DAX Formulas

The original dataset contained only raw transactional attributes. All business-critical metrics were engineered using **DAX**:

* **Total Sales** = `SUMX(Sales, Sales[Quantity] * Sales[List Price])`
* **Discount Rate** = `DIVIDE(TotalSalesByListPrice - TotalSales, TotalSalesByListPrice, 0)`
* **ASP (Average Selling Price)** = `DIVIDE([Total Sales], [Total Units])`
* **YoY Growth %** = `DIVIDE([Total Sales] - [Sales LY], [Sales LY])`

*Note: Used `DIVIDE` function for safe division to handle potential zero denominators.*

---

## 🛠️ Tech Stack

* **Tool:** Microsoft Power BI Desktop
* **Language:** DAX (Data Analysis Expressions)
* **Data Source:** Simulated Sales Data (Excel)
* **Techniques:** Data Modeling, ETL (Power Query), Data Visualization, Storytelling

---

## 📌 Next Steps (Engineering Roadmap)

* [ ] **Automation:** Integrate with **Power Automate** to trigger alerts when Sales drop below a threshold.
* [ ] **Scalability:** Migrate the backend from Excel to **Azure SQL Database** or **Databricks** for handling larger datasets.


---

*Author: Zoe Xia*
*[LinkedIn Profile](https://www.linkedin.com/in/zoe-xia-4b6307132/) | [GitHub Portfolio](https://github.com/SpaceZoe)*
