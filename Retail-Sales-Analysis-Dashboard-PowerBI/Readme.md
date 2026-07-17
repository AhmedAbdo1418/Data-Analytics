I developed this Sales Analysis Dashboard using Power BI to help management monitor sales performance and make data-driven decisions. I started by cleaning and transforming the data using Power Query, then designed a star schema data model. After that, I created DAX measures to calculate KPIs such as Total Sales, Total Cost, Number of Orders, Active Customers, and Best Sales Month. Finally, I built an interactive dashboard with slicers and visualizations to allow users to analyze sales trends across different years and business dimensions
Using Power Query, I :

Removed duplicates

Checked missing values
Changed data types
Standardized date formats
Removed unnecessary columns
Created Year and Month columns

Improved data quality
I Also Calculated Some KPIs

1.Total Sales = SUM(FactSales[Sales]) 
2.Number of Users = DISTINCTCOUNT(DimCustomer[CustomerID])
3.Total Cost = SUM(FactSales[Cost])
4.Active Users= DISTINCTCOUNT(FactSales[CustomerID])

5.Orders Number= COUNT(FactSales[OrderID])

6.Best Month
7.Sales by Month (Donut Chart)

Shows each month's contribution to total sales.
Management can immediately identify:
Strong months
Weak months
Seasonal patterns

8.Monthly Sales Trend

The Line Chart displays sales growth month by month.
Observations from your dashboard:
Sales increased gradually.
December achieved the highest sales.
February had relatively lower sales.
Growth accelerated during the last quarter.

9.Filters

The dashboard includes interactive slicers for:
Year
Product Category (if available)
Region
Customer Segment
Other business dimensions
Users can filter the dashboard instantly.

10.User Experience

The dashboard was designed to be:
Interactive
Simple
Executive-friendly
Fast
Easy to navigate

11.Business Insights

From this dashboard, management can conclude:
December generated the highest revenue.
Total sales reached 29.37M.
More than 60K orders were processed.
Around 18K customers made purchases.
Sales show an upward trend toward the end of the year.
Seasonal demand peaks in Q4.

Thanks, Ahmed Abdo
+201096702488





