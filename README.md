# Supermarket-Sales-Analysis
This Power BI project showcases end-to-end data analysis. It covers Power Query for cleaning raw supermarket sales data, DAX for creating key metrics like total sales and average tax, and dynamic dashboards with charts and KPIs to visualize performance by customer and month.
Supermarket Sales Analysis Dashboard
<p align="center">
<img src="images/dashboard-overview.png" alt="Supermarket Sales Dashboard Overview" width="800"/>
</p>

🚀 Project Overview
This project is a complete business intelligence solution for analyzing supermarket sales data using Power BI. The goal was to transform raw data into a dynamic and actionable dashboard, providing valuable insights into sales performance. The project was designed and executed based on a series of specific tasks, from data cleaning and analysis to designing an interactive dashboard.

🛠️ Tools and Technologies
Power BI Desktop: For modeling, analysis, and visual storytelling.

Power Query: For data cleaning and transformation.

DAX (Data Analysis Expressions): For creating custom measures and key performance indicators.

📊 Key Analyses and Insights
The dashboard was built to meet specific requirements and provide insights into:

Sales Performance: Tracking total sales, quantity, and tax.

Customer Analysis: Identifying total sales and order quantity per customer.

Time Trends: Visualizing total sales by month to identify seasonal patterns.

Shipping Efficiency: Calculating the average number of days to ship to determine operational efficiency.

⚙️ Workflow Breakdown
<details>
<summary><b>1. Data Cleaning and Preparation (Power Query)</b></summary>
<br>
The raw data was imported into the Power Query Editor, and the following steps were performed to ensure data quality:
<ul>
<li><b>Irrelevant Row Removal:</b> Removed empty or null rows from the bottom of the table.</li>
<li><b>Data Type Conversion:</b> Ensured all columns had the correct data types, such as converting date columns to the "Date" format and numeric columns to "Decimal Number" or "Whole Number".</li>
</ul>
</details>

<details>
<summary><b>2. Data Modeling and Analysis (DAX)</b></summary>
<br>
The following custom measures and columns were created using DAX to meet the analysis requirements:
<ul>
<li>Total Sales = <code>SUM('Sales'[Total (USD)])</code></li>
<li>Total Quantity = <code>SUM('Sales'[Order Quantity])</code></li>
<li>Average Retail Price = <code>AVERAGE('Sales'[Retail Price (USD)])</code></li>
<li>Average Order Quantity = <code>AVERAGE('Sales'[Order Quantity])</code></li>
<li>Average Tax = <code>AVERAGE('Sales'[Tax (USD)])</code></li>
<li>Days to Ship (<b>New Column</b>) = <code>DATEDIFF('Sales'[Order Date], 'Sales'[Ship Date], DAY)</code></li>
<li>Average Shipment Days = <code>AVERAGE('Sales'[Days to Ship])</code></li>
</ul>
</details>

<details>
<summary><b>3. Dashboard Design and Visualization</b></summary>
<br>
An interactive dashboard was designed to clearly display the insights, with a focus on specific visualization tasks:
<ul>
<li><b>Key Performance Indicators (KPIs):</b> Cards were created to show core metrics like Total Sales, Average Tax, and Average Order Quantity.</li>
<li><b>Analytical Charts:</b>
<ul>
<li>A bar chart showing Total Sales by Customer.</li>
<li>A column chart illustrating Total Sales per Month based on Order Date.</li>
<li>A table displaying Order Quantity per Customer.</li>
</ul>
</li>
</ul>
</details>
