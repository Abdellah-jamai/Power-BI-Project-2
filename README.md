# Customer & sales performance dashboard






https://github.com/user-attachments/assets/471a8e33-54e0-4766-972a-c0c0cabe5179






## 🔗 Project Overview

This project involves a comprehensive analysis of customer purchasing behavior using a dataset of 1,000 unique customers.
The goal was to transform raw sales data into actionable business segments insights about revenue variables, customer demographics, and loyalty.

## 🚀 Key Features & Insights

•	Revenue Performance: Real-time tracking of Total Revenue ($3.1M) and Average Order Value ($2,683).
•	Demographic Profiling: Visualized sales distribution across age groups, identifying the "50 and Above" segment as the primary revenue driver.
•	Customer Segmentation: Classified customers into VIP, Regular, and New segments to help target marketing efforts.
•	Retention Analysis: A scatter plot analysing the correlation between Recency (days since last purchase) and Total Sales to identify churn risks.

## 🛠️ Tools Used

•	SQL (SQL Server): Used for data extraction, cleaning, and complex aggregations (CTEs and Joins).
•	Power BI / DAX: For interactive data modeling and advanced time-intelligence calculations.
•	Power Query: For final data type transformations.

### Example: Calculating Revenue & Customer Metrics

SELECT 
    COUNT(DISTINCT Customer_key) AS Total_Customers,
    SUM(Total_sales) AS Total_Revenue,
    ROUND(AVG(Total_sales), 2) AS Avg_Order_Value
FROM gold_report_customers;

### Example: Segmenting Customers by Age Group

SELECT 
    CASE 
        WHEN age >= 50 THEN '50 and Above'
        WHEN age BETWEEN 40 AND 49 THEN '40-49'
        WHEN age BETWEEN 30 AND 39 THEN '30-39'
        ELSE 'Under 30'
    END AS Age_Group,
    SUM(Total_sales) AS Revenue_By_Group
FROM gold_report_customers
GROUP BY 1
ORDER BY Revenue_By_Group DESC;

## 📈 Technical DAX Highlights

To achieve the metrics shown in the dashboard, I implemented custom DAX measures including:
Code snippet
// Total Revenue Calculation
Revenue = SUM('Gold report customers'[Total_sales])

## Conclusion 

This project successfully transformed raw customer financial data into an interactive executive dashboard using a comprehensive data strategy with SQL and Power BI.
Using SQL for comprehensive data cleaning and aggregation, I created a high-performance basis for deep analytical exploration.
Key business drivers were discovered, including a total revenue of $3.1M and a high-value demographic concentration in the 50+ age segment.
I used extensive DAX analysis, I created dynamic KPIs that offer real-time visibility into customer loyalty and purchasing trends. 
The final dashboard provides actionable insights that allow decision-makers to optimize marketing strategies for VIP and high-spend groups.
Finally, this repository demonstrates a professional ability to navigate the entire data lifecycle from backend engineering to frontend business intelligence.



