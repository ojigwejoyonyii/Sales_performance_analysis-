#  SALES PERFORMANCE ANALYSIS

![Sales](https://github.com/ojigwejoyonyii/Sales_performance_analysis-/blob/main/Images/SALES.png)

---

# Table Of Content

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

# 🧹 Data Preparation, Cleaning and Validation

Before analysis, the raw dataset was reviewed and prepared to improve consistency and usability. The cleaning stage is important because analytical results depend on the quality and structure of the underlying data.

A. **Reviewed the raw dataset structure and column fields**. In other to understand the dataset, I first explored the column headers to understand the value held by each one and what such value meant.

B. **Checked the dataset for missing or incomplete values**. To check for null cells I clicked on the filter arrow on each column header and explored the content of each column to ensure there is no null cell or error value.

C. **Reviewed data types to ensure dates, numerical fields, and categorical fields were suitable for analysis**.  My major concern was the year column, the month column and the sales column. To ensure that the data type in this columns are valid I explored each column individually. For the month column I highlighted the column went to Home Tab and then to number group command to identify the format in which it was saved as and it was saved in general format, since the dataset did not provide full information about the date in which sales took place, such as providing the day, it just provided information on year and month so I left it in general format instead of changing it to short date or long date format. The exploration, result and decision I made in the year column also applies to the month column. For the sales column in other to ensure that the data in the column is valid I used the minimum function, since the sales values represent revenue generated from each sales then its value should never be a negative value which is why I used the minimum function. The formula I used is this (=MIN(Sales_info[Sales]) and it returned the value 196.25 showing that sales column doesn’t have a negative value.

D. **Checked for duplicate values**. I did not check for duplicate values in each column because of the nature of the dataset. The year column will definitely have values occurring more than once, given that multiple sales can be made in a particular year causing the year to appear more than once in the year column, this same explanation applies to the year column and the sales column. So I checked for duplicate value on the table as a whole by highlighting the table containing  the dataset, going to Data Tab, under data tools group command I selected remove duplicate and checked all the columns header and clicked ok,  the command returned no duplicate value found.

E. **Removed error sign**. To remove the error sign on the order# column I highlighted the whole column, clicked on the error icon and selected ignore error sign. I further investigated the cause of the error sign showing in the order# column and I discovered that error sign is showing because the column contains numerical value but was stored as text. During my analysis, when counting the number of orders in the order# column I simply used the COUNTA function. I adopted the COUNTA function solution in place of converting the column to be stored as numeric value.

F. **Renamed column**. For ease of understanding during analysis I changed the column header containing product types from Type to ProductType.

G. **Confirmed the number of records after cleaning**. I reviewed the total number of records before and after cleaning the sales dataset in other to access the impact of the cleanings I carried out and to ensure that the resulting dataset contained the expected number of records. Before I carried out any cleaning I explored the row header and discovered that on subtracting the column header that the sales_info table contains 444 populated cells/ records, I carried out the same exploration after cleaning and the still had 444 populated cells/records.

H. **Retained a separate cleaned dataset so that the transformation process could be distinguished from the original data**.

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

![DASHBOARD](https://github.com/ojigwejoyonyii/Sales_performance_analysis-/blob/main/Images/Sales-performance_analysis_dashboard.PNG)

---

# 💡 Key Findings and Insights 

This analysis revealed key insights into sales performance, regional performance, product performance and trends. The findings below highlight the most significant patterns and areas of performance identified from the data.

•	From the analysis I identified that revenue increased from **$428,437.00 to $480,267.00** in 2014 [12.1% increase] and fell to **$470,869.20** in 2015 which is about approximately **1.96%** decrease in revenue.

•	Three of the five salespersons Bishop, Lee and Parker consistently accounted for the highest revenue over the three year period. Their year on year rankings frequently changed, with each salesperson taking the lead at different points. This indicates a relatively competitive environment among the top performers, although further information will be needed to determine the factors driving this changes. Over the three years considered in this analysis Pullen generated the lowest revenue.

•	Central region generated the highest revenue consistently over three years, it generated a total sum of **$1,391,555.30** whereas the south region generated the lowest revenue over three years, it generated the sum of **$505,968.95**. 

•	April consistently recorded the highest revenue across the three year period. During this peak month, ice cream and tasty treats generated the highest revenue, followed by frozen yoghurt, while popsicles recorded significantly lower revenue than the other product types.

•	Popsicles recorded their highest revenue in May consistently across the three year period, despite being the lowest performing product in April. Regionally, Popsicles generated the lowest revenue in the north over three years while tasty treats recorded its weakest sales performance in the south.

---

# 🚀 Recommendations
Based on the analytical framework, the following actions are recommended for further business investigation:

•	Management could consider introducing clearly defined sales target and performance based incentives to encourage sustained sales performance. Targets could be set based on historical performance and adjusted to reflect market conditions while incentives could recognize both individual achievement and consistent performance over time.

•	Management should leverage the consistent April sales peak by increasing inventory and promotional activities for high performing products such as ice cream, tasty treats and frozen yoghurt ahead of the period. At the same time, the consistent low performance of Popsicles in April should be investigated to determine whether pricing, customer preference, product positioning, or availability is contributing to its weak sales.

•	Given that popsicles perform the highest in May over the three years considered in this analysis, management should consider increasing the inventory of popsicles around May period as well as promotional activities in other to take advantage of its consistent strong seasonal performance.

•	Management should investigate why popsicles underperform in the north and why tasty treats underperform in the south, factors like customers preference, pricing, local competition, and availability could be considered. Management could test targeted promotions or alternative pricing for popsicles in the north and tasty treats in the south to determine whether their performance can be improved.

•	Rather than applying one marketing strategy across the regions, promotions could be tailored to products that have stronger demand in each region.

---

# 🚧 Project Limitations

1. The analysis is limited to the fields available in the supplied dataset.

2. Revenue is analyzed, but the dataset does not provide enough information to assess profitability unless cost data is available.

3. The analysis describes observed patterns but does not establish causal relationships.

4. Salesperson differences should not be interpreted as individual effectiveness without considering territory size, customer mix, targets, and other contextual factors

---

# 🛠️ Tools 

|Tool / Technology	|Use in Project|
|-------------------|--------------|
Microsoft Excel	|Data preparation, calculations, analysis, visualization, and dashboard development.
Excel Tables / Worksheets	|Structured storage and organization of raw and cleaned data.
Formulas / Aggregation	|Calculation and summarization of sales measures.
Pivot table, pivot Charts and Dashboard	|Visual presentation of sales performance and trends.

---

# 🔄 Project Workflow

The project followed the workflow below:

•	Data Source → Obtain the original CSV dataset from link provided by the organization.

•	Data Ingestion → Import the CSV data into Excel.

•	Data Exploration → Review fields, records, data types, and available dimensions.

•	Data Cleaning → Correct, standardize, and prepare fields for analysis.

•	Data Validation → Check record counts, totals, dates, and data consistency.

•	Analysis → Aggregate sales by region, salesperson, product type, year, and month.

•	Visualization → Build charts and summary views.

•	Dashboard → Combine important KPIs and visuals into a management-friendly interface.

•	Insight Generation → Interpret observed patterns.

•	Documentation → Record the methodology, findings, limitations, and recommendations.

#  📂 Workbook Structure

The workbook is organized into separate areas for data preparation, analysis, and reporting. The exact worksheet names should be retained in the final documentation if the workbook is published alongside the project.

•	Raw sales data — 445 rows × 8 columns.

•	Revenue by region — 8 rows × 2 columns.

•	Revenue by salesperson — 9 rows × 2 columns.

•	Revenue by type — 8 rows × 2 columns.

•	Revenue by year — 7 rows × 2 columns.

•	Revenue by month — 11 rows × 2 columns.

•	Cleaned sales data — 445 rows × 8 columns.

•	DASHBOARD — 9 rows × 6 columns.

---

# 📝 Conclusion

The Sales Performance Analysis project demonstrates an end-to-end approach to working with sales data in Microsoft Excel. The project moves from raw transactional data through cleaning and validation to analysis, visualization, dashboard development, and business interpretation.

With 444 sales records covering the 2013–2015 period, the analysis provides a structured view of sales performance across regions, salespeople, product types, and time. The resulting dashboard provides a practical reporting tool for monitoring performance, while the supporting analysis creates a foundation for more detailed investigations.

Future versions of the project could be expanded by incorporating cost and profit data, customer segmentation, sales targets, discounts, profitability analysis, and automated refresh processes. These additions would allow the analysis to move beyond revenue reporting toward a broader business-performance perspective.

