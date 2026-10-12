![sales](https://github.com/ojigwejoyonyii/Sales_performance_analysis-/blob/main/Images/sales.jfif)

# 📊 SALES PERFORMANCE ANALYSIS

---

# 📝 PROJECT OVERVIEW

The Sales Performance Analysis project was developed to examine sales activity and performance across different business dimensions using Microsoft Excel. The analysis transforms a raw sales dataset into a structured, validated, and analysis-ready dataset and then uses summary calculations and visualizations to identify sales patterns, performance differences, and areas requiring attention.

The project follows a practical data-analysis workflow: data sourcing, data ingestion, data cleaning, data validation, analysis, visualization, interpretation, and recommendation. The final output is an Excel dashboard supported by detailed analytical worksheets.

---

# ❓ Business Problem

Sales data can contain valuable information about revenue generation, product performance, regional activity, salesperson contribution, and changes over time. However, raw transactional data does not immediately provide management with a clear view of these patterns.
The purpose of this project is therefore to organize and analyze the available sales records in order to answer practical business questions such as:

•	How much revenue was generated during the period covered by the dataset?

•	How are sales distributed across regions?

•	Which salespeople contribute most to recorded sales?

•	Which product types generate the highest sales?

•	How does sales performance change from year to year?

•	Which months show stronger or weaker sales activity?

•	What patterns can be observed that may support future sales planning?

---

# 🎯 Project Objectives

This project was designed to examine sales performance across key dimensions, identify trends and areas of improvement and to generate meaningful insights that can support data driven business decisions. The following objectives guided the analysis;

•	Calculate and summarize key sales performance measures.

•	Compare sales performance across regions, salespeople, product types, years, and months.

•	Develop clear visualizations that make important sales patterns easy to understand.

•	Create an interactive Excel dashboard that provides a concise management-level view of performance.

•	Translate analytical results into practical business insights and recommendations.

---

# 🔍 Project Scope

The project covers the period of 2013 to 2015 (3 years) and focuses on the following areas:

•	Overall sales performance

•	Regional sales performance

•	Salesperson performance

•	Product-type performance

•	Annual sales trends

•	Monthly sales trends

•	Dashboard-based presentation of key findings

The project is descriptive and diagnostic in nature. It focuses on understanding what happened in the available sales data and identifying observable patterns. It does not attempt to build a predictive sales forecast or a causal model.

---

# 📂 Data Source And Description

The dataset utilized for this project was obtained through a source provided by the organization. The organization supplied the reference link from which the dataset was accessed and downloaded in CSV format. The dataset was then imported into Microsoft Excel for data preparation, cleaning, validation, analysis, and visualization.

[raw dataset link](https://docs.google.com/spreadsheets/d/1fjp30qHIWajY6D_LttBm194fUu2ZTB3e/edit?usp=drive_link&ouid=110086479642571627068&rtpof=true&sd=true)

The dataset utilized for this project was obtained through a source provided by the organization and is presented in CSV format. 
|Dataset Attribute|	Value|
|-----------------|-------|
Number of sales records|	444
Total units recorded	|2,322,594
Total sales revenue	|3,254,576.95
Date coverage	|2013–2015
Primary analysis tool	|Microsoft Excel
Source format|	CSV
Column headers	|Year, Month, ProductType, Salesperson, Region, Sales, Units, Order#

The workbook contains 444 sales records and covers three calendar years, 2013 through 2015. The dataset records approximately 2.32 million units and total sales revenue of approximately 3.25 million.

The dataset utilized for this project was obtained through a source provided by the organization and is presented in CSV format. 
Dataset Attribute	Value
Number of sales records	444
Total units recorded	2,322,594
Total sales revenue	3,254,576.95
Date coverage	2013–2015
Primary analysis tool	Microsoft Excel
Source format	CSV
Column headers	Year, Month, ProductType, Salesperson, Region, Sales, Units, Order#

The workbook contains 444 sales records and covers three calendar years, 2013 through 2015. The dataset records approximately 2.32 million units and total sales revenue of approximately 3.25 million.

---

# ⚙️ Analytical Methodology

This analysis was performed using aggregation, grouping, comparison, and visualization techniques in Excel. Sales records were summarized across selected dimensions to reveal differences in performance.

|Analysis Dimension|	Purpose|
|------------------|---------|
Region	       |Compare geographic or regional contribution to total sales.
Salesperson	   |Identify differences in individual sales contribution.
Product Type   |Determine which product categories generate more sales.
Year	Examine  |annual changes in sales performance.
Month	Identify | monthly patterns and periods of stronger or weaker sales activity.

---

# Key Performance Indicators

This project uses the following core measures to describe sales performance:

|KPI	|Definition	|Purpose	|Formula Used|
|-----|-----------|---------|------------|
Total Sales Revenue  |Sum of recorded sales values.  |	Measures overall revenue generated.|	=SUM(Sales_info[Sales])|
Total Units Sold   |Sum of recorded quantities/units.	|Measures sales volume.|	=SUM(Sales_info[Units])
Number of Orders/Records|	Count of sales transactions represented in the dataset.|	Provides a measure of transaction activity.	|=COUNTA(Sales_info[Order’#])|
Sales by Region	|Sales aggregated by region.|	Shows regional contribution. |Gotten by dragging Region to the category axis of the pivot table and Total Sales Revenue to the value axis|
Sales by Salesperson	|Sales aggregated by salesperson.	|Shows individual contribution.	|Gotten  by dragging Salesperson to the category axis of the pivot table and Total Sales Revenue to the value axis
Sales by Product Type	|Sales aggregated by product category/type.|	Shows product performance. |Gotten  by dragging Product to the category axis of the pivot table and Total Sales Revenue to the value axis|
Sales by Year	|Sales aggregated by calendar year.|	Shows annual trend. |Gotten  by dragging Year to the category axis of the pivot table and Total Sales Revenue to the value axis|
Sales by Month	|Sales aggregated by month.	|Shows seasonal/monthly pattern.	|Gotten  by dragging Month to the category axis of the pivot table and Total Sales Revenue to the value axis|

---

# Dashboard Development

An Excel dashboard was developed to consolidate the main findings into a single visual reporting interface. The dashboard is designed to make the most important sales information accessible without requiring the user to inspect every underlying worksheet.
The dashboard brings together information relating to:

•	Overall sales performance

•	Regional performance

•	Salesperson performance

•	Product-type performance

•	Annual sales trends

•	Monthly sales trends

The dashboard also contains 4 slicers which includes Region, Year, Salesperson, and Type. These slicers makes the dashboard interactive, because of the connection created between the slicers and the charts. Also the slicers enables exploring and answering of business questions that are not glaring from the charts but can be gotten by using the slicers.
The dashboard serves as the presentation layer of the project, while the cleaned data and supporting analysis worksheets provide the underlying calculations.
