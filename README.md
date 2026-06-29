# DSA3050A_MidSem_Merhawit_670554
Business Intelligence &amp; Visualization
---
# DSA3050A_MidSem_Merhawit_670554

## Global Superstore Sales Dashboard
### Business Intelligence & Visualization — Mid Semester Practical Examination

---

## Student Information
| Field | Details |
|---|---|
| **Student Name** | Merhawit Kassa |
| **Student ID** | 670554 |
| **Course** | DSA 3050A — Business Intelligence & Visualization |
| **Examination** | Mid Semester Practical Examination |
| **Submission** | Public GitHub Repository |

---

## Introduction
This project presents a comprehensive Business Intelligence solution developed for a global retail organization using the Global Superstore dataset. As a Business Intelligence Analyst, the task involved receiving a large raw dataset containing errors, inconsistencies, missing values, and poorly structured fields. The dataset was cleaned and transformed using Power Query in Power BI Desktop, and a professional interactive dashboard was developed to support management decision-making.

The dashboard provides insights into sales performance, regional profitability, customer segmentation, and sales trends across four years of transaction data (2011–2014).

---

## Dataset Information
| Field | Details |
|---|---|
| **Dataset Name** | Global Superstore Sales Dataset |
| **Source** | Kaggle — https://www.kaggle.com/datasets/anandaramg/global-superstore |
| **Original Rows** | 51,291 rows |
| **Columns** | 24 columns (23 after cleaning) |
| **Time Period** | 2011 — 2014 |
| **Format** | Excel (.xlsx) |

### Dataset Columns Include:
- Order ID, Order Date, Ship Date, Ship Mode
- Customer Name, Segment, Region, Country, City, State
- Category, Sub-Category, Product Name
- Sales, Profit, Quantity, Discount, Shipping Cost
- Market, Order Priority

---

## Business Problem
Management requires a data-driven dashboard to answer the following business questions:
1. What are the overall sales, profit, and quantity trends?
2. Which regions are most and least profitable?
3. Which customer segments drive the most revenue?
4. How do sales trends vary across quarters and years?
5. Which product categories generate the most sales?

---

## Repository Structure

DSA3050A_MidSem_Merhawit_670554/

│

├── Dataset/

│   └── dataset.xlsx          — Raw Superstore dataset from Kaggle

│

├── PBIX/

│   └── MidSemExam.pbix       — Power BI dashboard file

│

├── Screenshots/

│   ├── raw_dataset.png               — Raw imported dataset

│   ├── power_query_editor.png        — Power Query Editor view

│   ├── applied_steps.png             — Applied Steps pane

│   ├── column_profile.png            — Column profiling results

│   ├── final_cleaned_dataset.png     — Final cleaned dataset

│   ├── renamed_columns.png           — Renamed unclear columns

│   ├── data_types.png                — Changed data types

│   ├── removed_duplicates.png        — Removed duplicate records

│   ├── blank_rows.png                — Removed blank rows

│   ├── trim_clean.png                — Trimmed and cleaned text

│   ├── replaced_values.png           — Replaced inconsistent values

│   ├── removed_columns.png           — Removed unnecessary columns

│   ├── split_column.png              — Split Order ID column

│   ├── merged_column.png             — Merged City and Country

│   ├── custom_column.png             — Profit Margin % column

│   ├── conditional_column.png        — Sales Performance column

│   ├── date_extraction.png           — Year, Month, Quarter, Day

│   ├── filtered_rows.png             — Filtered rows (2 conditions)

│   ├── sorted_data.png               — Sorted data

│   ├── index_column.png              — Added index column

│   ├── group_by.png                  — Group By aggregations

│   ├── extract_text.png              — Text Before Delimiter

│   ├── date_table.png                — Date Table created

│   ├── nested_conditional.png        — Business Categories

│   ├── cover_page.png                — Dashboard cover page

│   ├── dashboard.png                 — Full dashboard view

│   ├── slicers.png                   — Three slicers added

│   ├── drill_year.png                — Drill down Year level

│   ├── drill_quarter.png             — Drill down Quarter level

│   ├── cross_filter_before.png       — Before cross filtering

│   └── cross_filter_after.png        — After cross filtering

│

├── README.md                 — Project documentation

└── Insights.pdf              — Business insights report

## Power Query Transformations Performed

### A. Basic Data Cleaning
| # | Transformation | Details |
|---|---|---|
| 1 | **Renamed Columns** | Renamed 记录数→Record Count, Row ID→Row Number, weeknum→Week Number, Market2→Market Group |
| 2 | **Changed Data Types** | Order Date & Ship Date→Date, Sales/Profit/Discount→Decimal, Quantity→Whole Number |
| 3 | **Removed Duplicates** | Removed duplicate records based on Order ID |
| 4 | **Removed Blank Rows** | Removed all blank rows and null values from key columns |
| 5 | **Trimmed & Cleaned Text** | Applied Trim and Clean on Customer Name, Product Name, Category, Segment, Region |
| 6 | **Replaced Inconsistent Values** | Standardized Ship Mode values (Same Day→Same-Day, First Class→First-Class) |
| 7 | **Removed Unnecessary Columns** | Removed Record Count, Row Number, Customer ID, Product ID, Postal Code |

### B. Intermediate Transformations
| # | Transformation | Details |
|---|---|---|
| 1 | **Split Column** | Split Order ID into Order Country Code, Order Year, Order Number |
| 2 | **Merge Columns** | Merged City and Country into City, Country column |
| 3 | **Custom Column** | Created Profit Margin % = Profit / Sales * 100 |
| 4 | **Conditional Column** | Created Sales Performance (High/Medium/Low/Very Low) |
| 5 | **Date Extraction** | Extracted Year, Month, Quarter, Day from Order Date |
| 6 | **Filter Rows** | Filtered Sales > 0 AND Order Priority ≠ Low |
| 7 | **Sort Data** | Sorted by Order Date Ascending then Sales Descending |
| 8 | **Index Column** | Added Record ID index column starting from 1 |

### C. Advanced Power Query Tasks
| # | Task | Details |
|---|---|---|
| 1 | **Group By** | Created Sales Summary with Total Sales, Profit, Quantity, Average Discount by Category |
| 2 | **Extract Text** | Extracted Product Brand using Text Before Delimiter |
| 3 | **Date Table** | Created full Date Table (2011–2014) with Year, Month, Quarter, Day, Month Name |
| 4 | **Nested Conditional Logic** | Created Business Category column (High Value Profitable/Loss Making, Low Value Profitable/Loss Making) |
| 5 | **Column Profiling** | Used Column Quality, Distribution, and Profile to identify data quality issues |

---

## Dashboard Visuals Created

| # | Visual | Description |
|---|---|---|
| 1 | **KPI Card — Total Sales** | Shows overall total sales value |
| 2 | **KPI Card — Total Profit** | Shows overall total profit value |
| 3 | **KPI Card — Total Quantity** | Shows total quantity of items sold |
| 4 | **Bar Chart** | Sales by Category |
| 5 | **Column Chart** | Profit by Region |
| 6 | **Line Chart** | Sales Trend Over Time (with drill down) |
| 7 | **Donut Chart** | Sales by Segment |
| 8 | **Table Visual** | Order Details (Customer, Sales, Profit, Region) |
| 9 | **Matrix Visual** | Sales & Profit by Category and Region |
| 10 | **Map Visual** | Sales by Country (bubble map) |
| 11 | **Treemap** | Sales by Sub-Category |
| 12 | **Scatter Chart** | Sales vs Profit Analysis |

---

## Dashboard Interactivity

| Feature | Details |
|---|---|
| **Slicer 1** | Filter by Year |
| **Slicer 2** | Filter by Category |
| **Slicer 3** | Filter by Region |
| **Drill Down** | Line Chart — Year → Quarter → Month → Day |
| **Cross Filtering** | Clicking any visual filters all other visuals |

---

## Business Insights

### Insight 1 — Q4 Drives Peak Revenue Performance
Analysis of the Sales Trend Over Time chart reveals a strong and consistent upward pattern in sales throughout the year. Sales begin at 36K in Q1, gradually increasing to 74K in Q2 and 85K in Q3, before reaching a peak of 117K in Q4 — representing a 225% growth from Q1 to Q4. This pattern strongly suggests that customer purchasing behavior is heavily influenced by end-of-year factors such as holiday seasons, promotional campaigns, and budget spending cycles. Management should plan ahead by increasing stock levels, hiring seasonal staff, and launching targeted marketing campaigns before Q4 to fully capitalize on this peak demand period.

### Insight 2 — Consumer Segment Dominates Revenue
The Sales by Segment donut chart clearly shows that the Consumer segment is the primary revenue driver, contributing 56.63% of total sales, followed by Corporate at 28.54% and Home Office at 14.83%. This indicates that the majority of the organization's customer base consists of individual consumers rather than business clients. While the Consumer segment is performing strongly, the Home Office segment at only 14.83% represents a significant growth opportunity. Management should consider developing specialized product bundles, pricing strategies, and targeted marketing campaigns aimed at Home Office customers to grow this underperforming segment and diversify the revenue base.

### Insight 3 — EMEA Region Requires Urgent Attention
The Profit by Region chart reveals significant variation in profitability across different regions. Central Region leads with the highest profit of 80K, closely followed by North at 79K, North Asia at 58K, and Oceania at 50K. However, EMEA is the only region recording a negative profit of -5K, making it the only loss-making region requiring immediate management attention. The consistent losses in EMEA could be attributed to high operational costs, excessive discounting, or unfavorable market conditions. It is recommended that management conducts a detailed cost-benefit analysis of EMEA operations, reviews the current pricing and discount strategies, and considers restructuring the sales approach to return EMEA to profitability.

---

## Tools Used
- **Power BI Desktop** — Data transformation and dashboard development
- **Power Query** — Data cleaning and transformation
- **Microsoft Excel** — Raw dataset format
- **GitHub** — Version control and submission

---

*Submitted for DSA 3050A — Business Intelligence & Visualization*
*Mid Semester Practical Examination*
*Merhawit Kassa | Student ID: 670554*
