# 📊 Sales Performance Analysis

> **An end-to-end Excel data analysis project that transforms raw sales records into a cleaned, validated dataset, supporting analysis worksheets, and an interactive management dashboard.**

![Tool](https://img.shields.io/badge/Tool-Microsoft%20Excel-217346?logo=microsoftexcel&logoColor=white)
![Data](https://img.shields.io/badge/Data-CSV-blue)
![Period](https://img.shields.io/badge/Period-2013--2015-orange)
![Type](https://img.shields.io/badge/Analysis-Descriptive%20%26%20Diagnostic-lightgrey)

---

## 📑 Table of Contents

- [Project Overview](#-project-overview)
  
- [Business Problem](#-business-problem)
  
- [Project Objectives](#-project-objectives)
  
- [Project Scope](#-project-scope)
  
- [Dataset Overview](#️-dataset-overview)
  
- [Data Source](#-data-source)
  
- [Data Preparation, Cleaning and Validation](#-data-preparation-cleaning-and-validation)
  
- [Analytical Methodology](#-analytical-methodology)
  
- [Key Performance Indicators](#-key-performance-indicators)
  
- [Analysis Performed](#-analysis-performed)
  
  - [Regional Sales Analysis](#regional-sales-analysis)
    
  - [Salesperson Performance Analysis](#salesperson-performance-analysis)
    
  - [Product-Type Analysis](#product-type-analysis)
    
  - [Yearly Sales Analysis](#yearly-sales-analysis)
    
  - [Monthly Sales Analysis](#monthly-sales-analysis)
    
- [Dashboard Development](-#️dashboard-development)
  
- [Key Findings and Insights](#-key-findings-and-insights)
  
- [Recommendations](#-recommendations)
  
- [Project Limitations](#️-project-limitations)
  
- [Tools](#️-tools)
  
- [Project Workflow](#-project-workflow)
  
- [Workbook Structure](#-workbook-structure)
  
- [Conclusion](#-conclusion)
  
- [Future Improvements](#-future-improvements)
  
- [Appendix A: Data Dictionary](#-appendix-a-data-dictionary)


---

## 🔍 Project Overview

The Sales Performance Analysis project examines sales activity and performance across different business dimensions using Microsoft Excel. It transforms a raw sales dataset into a structured, validated, and analysis-ready dataset, then uses summary calculations and visualizations to identify sales patterns, performance differences, and areas requiring attention.

The project follows a practical data-analysis workflow:

**Data sourcing → Ingestion → Cleaning → Validation → Analysis → Visualization → Interpretation → Recommendation**

The final output is an Excel dashboard supported by detailed analytical worksheets.

---

## 💼 Business Problem

Sales data contains valuable information about revenue generation, product performance, regional activity, salesperson contribution, and changes over time. However, raw transactional data does not immediately give management a clear view of these patterns.

This project organizes and analyzes the available sales records to answer practical business questions:

- How much revenue was generated during the period covered by the dataset?
- How are sales distributed across regions?
- Which salespeople contribute most to recorded sales?
- Which product types generate the highest sales?
- How does sales performance change from year to year?
- Which months show stronger or weaker sales activity?
- What patterns can support future sales planning?

---

## 🎯 Project Objectives

- Calculate and summarize key sales performance measures.
- Compare sales performance across regions, salespeople, product types, years, and months.
- Develop clear visualizations that make important sales patterns easy to understand.
- Create an interactive Excel dashboard that provides a concise, management-level view of performance.
- Translate analytical results into practical business insights and recommendations.

---

## 🧭 Project Scope

The project covers **2013 to 2015 (3 years)** and focuses on:

- Overall sales performance
- Regional sales performance
- Salesperson performance
- Product-type performance
- Annual sales trends
- Monthly sales trends
- Dashboard-based presentation of key findings

> **Note:** The project is *descriptive and diagnostic* in nature. It explains what happened in the available data and identifies observable patterns. It does **not** build a predictive forecast or a causal model.

---

## 🗂️ Dataset Overview

| Dataset Attribute | Value |
| --- | --- |
| Number of sales records | 444 |
| Total units recorded | 2,322,594 |
| Total sales revenue | 3,254,576.95 |
| Date coverage | 2013–2015 |
| Primary analysis tool | Microsoft Excel |
| Source format | CSV |
| Column headers | `Year`, `Month`, `ProductType`, `Salesperson`, `Region`, `Sales`, `Units`, `Order#` |

---

## 🔗 Data Source

The dataset was provided by the organization through a reference link, downloaded in CSV format, and imported into Microsoft Excel for preparation, cleaning, validation, analysis, and visualization.

**Data source link:** [Google Sheets dataset](https://docs.google.com/spreadsheets/d/1fjp30qHIWajY6D_LttBm194fUu2ZTB3e/edit?usp=sharing&ouid=110086479642571627068&rtpof=true&sd=true)

---

## 🧹 Data Preparation, Cleaning and Validation

The raw dataset was reviewed and prepared to improve consistency and usability, since analytical results depend on data quality.

1. **Reviewed the raw dataset structure and column fields.**
   Explored each column header to understand the values it holds and what they mean.

2. **Checked for missing or incomplete values.**
   Used the filter arrow on each column header to inspect its contents and confirm there were no blank cells or error values.

3. **Reviewed data types.**
   The main concerns were the `Year`, `Month`, and `Sales` columns.
   - **Year / Month:** Checked via *Home → Number* group; both were stored in *General* format. Because the dataset provides only year and month (no day), they were left in General format rather than converted to a date format.
   - **Sales:** Revenue should never be negative, so the minimum was checked with `=MIN(Sales_info[Sales])`, which returned **196.25**, confirming no negative values.

4. **Checked for duplicates.**
   Individual columns were not checked, since repeated values in `Year`, `Month`, or `Sales` are expected. Instead, duplicates were checked across the whole table (*Data → Remove Duplicates*, all columns selected). **No duplicates were found.**

5. **Removed the error indicator on `Order#`.**
   The error flag appeared because numeric values were stored as text. Rather than converting the column, the *Ignore Error* option was applied and `COUNTA` was used to count orders.

6. **Renamed a column.**
   `Type` was renamed to `ProductType` for clarity during analysis.

7. **Confirmed record counts after cleaning.**
   The `Sales_info` table contained **444 records** both before and after cleaning.

8. **Retained a separate cleaned dataset.**
   The raw and cleaned data are kept apart so the transformation process remains distinguishable from the original data.

---

## 🧪 Analytical Methodology

The analysis uses aggregation, grouping, comparison, and visualization techniques in Excel. Sales records were summarized across the following dimensions:

| Analysis Dimension | Purpose |
| --- | --- |
| Region | Compare geographic or regional contribution to total sales. |
| Salesperson | Identify differences in individual sales contribution. |
| Product Type | Determine which product categories generate more sales. |
| Year | Examine annual changes in sales performance. |
| Month | Identify monthly patterns and periods of stronger or weaker sales activity. |

---

## 📐 Key Performance Indicators

| KPI | Definition | Purpose | Formula / Method |
| --- | --- | --- | --- |
| Total Sales Revenue | Sum of recorded sales values | Measures overall revenue generated | `=SUM(Sales_info[Sales])` |
| Total Units Sold | Sum of recorded quantities/units | Measures sales volume | `=SUM(Sales_info[Units])` |
| Number of Orders/Records | Count of sales transactions | Measures transaction activity | `=COUNTA(Sales_info[Order#])` |
| Sales by Region | Sales aggregated by region | Shows regional contribution | Pivot table: `Region` → Rows, Total Sales Revenue → Values |
| Sales by Salesperson | Sales aggregated by salesperson | Shows individual contribution | Pivot table: `Salesperson` → Rows, Total Sales Revenue → Values |
| Sales by Product Type | Sales aggregated by product category | Shows product performance | Pivot table: `ProductType` → Rows, Total Sales Revenue → Values |
| Sales by Year | Sales aggregated by calendar year | Shows annual trend | Pivot table: `Year` → Rows, Total Sales Revenue → Values |
| Sales by Month | Sales aggregated by month | Shows seasonal/monthly pattern | Pivot table: `Month` → Rows, Total Sales Revenue → Values |


---

## 📈 Analysis Performed

### Regional Sales Analysis
Compares total sales across regions to show where the business generates the greatest share of revenue and whether sales are concentrated in particular locations. Results can support decisions on sales coverage, resource allocation, territory management, and regional performance monitoring.

![REVENUE BY REGION](https://github.com/ojigwejoyonyii/Sales_performance_analysis-/blob/main/Images/Revenue_by_region-pivot%20table%20and%20chart.PNG)

### Salesperson Performance Analysis
Aggregates sales by individual salesperson. The goal is to understand the *distribution* of contribution across the team, not just identify high and low values. It can support performance discussions, target setting, coaching, and identifying sales practices worth investigating.

![REVENUE BY SALESPERSON](https://github.com/ojigwejoyonyii/Sales_performance_analysis-/blob/main/Images/Revenue_by_salespersons_pivot%20table%20and%20chart.PNG)

### Product-Type Analysis
Compares sales across product categories to reveal which account for the largest share of revenue and which may need review. Results should be read alongside unit volume, pricing, availability, and customer demand, since sales value alone does not explain a product's performance.

![REVENUE BY PRODUCT TYPE](https://github.com/ojigwejoyonyii/Sales_performance_analysis-/blob/main/Images/Revenue-by_product_type_pivot%20table%20and%20chart.PNG)

### Yearly Sales Analysis
Compares performance across 2013, 2014, and 2015 to give a high-level view of growth, decline, or stability. Comparisons involving an incomplete year should be interpreted carefully.

![REVENUE BY YEAR](https://github.com/ojigwejoyonyii/Sales_performance_analysis-/blob/main/Images/Revenue-by_year_pivot%20table%20and%20chart.PNG)

### Monthly Sales Analysis
Breaks sales into individual months to reveal recurring patterns hidden by annual totals. Useful for inventory planning, staffing, promotional planning, and sales target setting.

![REVENUE BY MONTH](https://github.com/ojigwejoyonyii/Sales_performance_analysis-/blob/main/Images/Revenue_by_month_pivot%20table%20and%20chart.PNG)


---

## 🖥️ Dashboard Development

An Excel dashboard consolidates the main findings into a single visual reporting interface, so users don't need to inspect every underlying worksheet. It covers:

- Overall sales performance
- Regional performance
- Salesperson performance
- Product-type performance
- Annual sales trends
- Monthly sales trends

**Interactivity:** The dashboard includes **4 slicers: `Region`, `Year`, `Salesperson`, and `Type`**. These are connected to the charts, allowing users to explore and answer business questions that are not obvious from the static visuals.

The dashboard is the presentation layer of the project, while the cleaned data and supporting worksheets hold the underlying calculations.

![SALES PERFORMANCE ANALYSIS DASHBOARD](https://github.com/ojigwejoyonyii/Sales_performance_analysis-/blob/main/Images/Sales-performance_analysis_dashboard.PNG)


---

## 💡 Key Findings and Insights

- **Revenue trend:** Revenue rose from **$428,437.00 (2013)** to **$480,267.00 (2014)**, a **12.1% increase**, then fell to **$470,869.20 (2015)**, a decrease of about **1.96%**.
- **Salesperson performance:** Three of the five salespeople, **Bishop, Lee, and Parker**, consistently accounted for the highest revenue over the three years. Their year-on-year rankings changed frequently, with each taking the lead at different points, which suggests a competitive environment among top performers. **Pullen** generated the lowest revenue overall. More information is needed to determine what drives these changes.
- **Regional performance:** The **Central** region consistently generated the highest revenue, totaling **$1,391,555.30** over three years. The **South** region generated the lowest, at **$505,968.95**.
- **Seasonal peak:** **April** consistently recorded the highest revenue across the three years. In that month, **ice cream** and **tasty treats** generated the most revenue, followed by **frozen yoghurt**, while **popsicles** were significantly lower.
- **Popsicle pattern:** Popsicles consistently peaked in **May**, despite being the weakest product in April. Regionally, popsicles were weakest in the **North**, and tasty treats were weakest in the **South**.

---

## ✅ Recommendations

Based on the analysis, the following actions are recommended for further business investigation:

1. **Set targets and incentives.** Introduce clearly defined sales targets and performance-based incentives, based on historical performance and adjusted for market conditions. Incentives could recognize both individual achievement and consistency over time.
2. **Capitalize on the April peak.** Increase inventory and promotional activity for high performers (ice cream, tasty treats, frozen yoghurt) ahead of April. Investigate popsicles' weak April performance (pricing, preference, positioning, or availability).
3. **Capitalize on the May popsicle peak.** Increase popsicle inventory and promotions around May to take advantage of its consistent seasonal strength.
4. **Investigate regional weaknesses.** Look into why popsicles underperform in the North and tasty treats in the South (customer preference, pricing, local competition, availability). Test targeted promotions or alternative pricing in those areas.
5. **Tailor regional marketing.** Rather than applying one strategy everywhere, tailor promotions to the products with stronger demand in each region.

---

## ⚠️ Project Limitations

- The analysis is limited to the fields available in the supplied dataset.
- Revenue is analyzed, but without cost data, **profitability cannot be assessed**.
- The analysis describes observed patterns but does **not** establish causal relationships.
- Salesperson differences should not be read as individual effectiveness without considering territory size, customer mix, targets, and other context.

---

## 🛠️ Tools

| Tool / Technology | Use in Project |
| --- | --- |
| Microsoft Excel | Data preparation, calculations, analysis, visualization, and dashboard development |
| Excel Tables / Worksheets | Structured storage and organization of raw and cleaned data |
| Formulas / Aggregation | Calculation and summarization of sales measures |
| Pivot Tables, Pivot Charts and Dashboard | Visual presentation of sales performance and trends |

---

## 🔄 Project Workflow

```text
Data Source → Data Ingestion → Data Exploration → Data Cleaning → Data Validation
     → Analysis → Visualization → Dashboard → Insight Generation → Documentation
```

| Stage | Description |
| --- | --- |
| Data Source | Obtain the original CSV dataset from the online source |
| Data Ingestion | Import the CSV data into Excel |
| Data Exploration | Review fields, records, data types, and available dimensions |
| Data Cleaning | Correct, standardize, and prepare fields for analysis |
| Data Validation | Check record counts, totals, dates, and data consistency |
| Analysis | Aggregate sales by region, salesperson, product type, year, and month |
| Visualization | Build charts and summary views |
| Dashboard | Combine key KPIs and visuals into a management-friendly interface |
| Insight Generation | Interpret observed patterns |
| Documentation | Record methodology, findings, limitations, and recommendations |

---

## 📁 Workbook Structure

The workbook is organized into separate areas for data preparation, analysis, and reporting.

| Worksheet | Dimensions |
| --- | --- |
| Raw sales data | 445 rows × 8 columns |
| Revenue by region | 8 rows × 2 columns |
| Revenue by salesperson | 9 rows × 2 columns |
| Revenue by type | 8 rows × 2 columns |
| Revenue by year | 7 rows × 2 columns |
| Revenue by month | 11 rows × 2 columns |
| Cleaned sales data | 445 rows × 8 columns |
| DASHBOARD | 9 rows × 6 columns |

> Row counts include the header row (444 records + 1 header = 445).

---

## 🏁 Conclusion

This project demonstrates an end-to-end approach to working with sales data in Microsoft Excel: from raw transactional data through cleaning and validation, to analysis, visualization, dashboard development, and business interpretation.

With 444 sales records covering 2013–2015, the analysis gives a structured view of sales performance across regions, salespeople, product types, and time. The dashboard provides a practical tool for monitoring performance, and the supporting analysis forms a foundation for deeper investigation.

### 🚀 Future Improvements

- Incorporate cost and profit data for profitability analysis
- Add customer segmentation
- Include sales targets and discount data
- Automate data refresh processes

---

## 📖 Appendix A: Data Dictionary

| Field | Description |
| --- | --- |
| `Year` | The year in which sales were made (from the original dataset) |
| `Month` | The month in which sales were made (from the original dataset) |
| `Type` (renamed `ProductType`) | The product types sold by the company (from the original dataset) |
| `Salesperson` | Name of the individual/employee who made the sale |
| `Region` | Geographical or business region associated with the sale |
| `Sales` | Monetary value associated with the recorded sale |

