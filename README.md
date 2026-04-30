# McCarthy-Uniform-Inventory-Analysis
Business Problem:
McCarthy Uniforms generates strong annual revenue from private school uniforms and kits; however, its inventory management system faces critical inefficiencies. A significant portion of merchandise experiences slow sales, leading to excess inventory and capital being tied up in low-performing SKUs. At the same time, high-demand items frequently go out of stock, resulting in missed sales opportunities and customer dissatisfaction.
The problem is further intensified by long supplier lead times (30–90 days), as products are manufactured overseas. This makes it difficult to respond quickly to demand fluctuations. The current inventory strategy does not effectively differentiate between high-value, fast-moving items and low-demand products, leading to both overstocking and stockouts.
Additionally, the lack of dynamic demand forecasting and adaptive reorder policies creates a mismatch between supply and actual demand patterns. As a result, the company struggles to maintain optimal inventory levels, impacting service levels, revenue potential, and operational efficiency.

Inventory Analysis Project – One Year Weekly Analysis (2019–2020)
📋 Project Overview
This project presents a comprehensive one-year inventory analysis conducted on weekly basis from 18 June 2019 to 18 June 2020. The objective was to analyze inventory performance, classify products using ABC-XYZ analysis, identify critical inventory issues, and provide actionable recommendations for inventory policy and forecasting.

🎯 Objectives

Perform ABC analysis based on revenue contribution (Pareto Principle)
Conduct XYZ analysis to measure demand variability and predictability
Combine ABC and XYZ analysis to create an ABC-XYZ Matrix
Identify current inventory health issues (Stockouts, Reorder Point violations, etc.)
Analyze inventory turnover by demand variability segments
Provide strategic recommendations for high-value, high-variability SKUs
Develop demand forecasting insights


📊 Key Findings
1. ABC Analysis (Revenue Contribution)

34 items (11.22% of total products) generated 291 million in revenue
51 items generated 85 million in revenue
218 items generated 42 million in revenue

→ 11.22% of products contributed 69.6% of total revenue, strongly validating the Pareto Principle (80/20 rule).
2. Current Inventory Health

280 items (92.4%) are below reorder point
10 items (3.3%) are completely out of stock and require immediate replenishment

3. ABC-XYZ Matrix Analysis
High-value products (Class A) show the following demand patterns:

Uniform demand: 27.6 million
Variable demand: 13.5 million
Uncertain demand: 5.94 million

Average Inventory Turnover Ratio across the portfolio: 5.4
Notably, AY SKUs (High Value + Variable Demand) generated 158.62 million in annual revenue.
4. Demand Forecasting
Using one year of weekly data (June 2019 – June 2020) with quarterly seasonality (13 weeks):

Point Forecast: 251,604 units per week
95% Confidence Interval:
Lower Bound: 114,573 units
Upper Bound: 388,635 units

Uncertainty Spread: ±137,031 units (Symmetric)

Key Observation: The wide confidence interval reflects the limitation of fitting a seasonal model on only one annual cycle.

🔍 Methodology
Data Processing

Weekly sales and demand calculated using DAX (CALCULATE, FILTER)
Weekly sales amount retrieved using LOOKUPVALUE
Average weekly demand and Standard Deviation calculated per SKU
Coefficient of Variation (CV) calculated to measure demand variability
Product-wise CV ranks created for XYZ Analysis

Analysis Techniques

ABC Analysis: Based on annual revenue and cumulative revenue share
XYZ Analysis: Based on Coefficient of Variation of weekly demand
ABC-XYZ Matrix: Combined classification
Data modeling with relationships on SKU_ID


📌 Strategic Recommendations
For AY SKUs (High Value + Variable Demand)

Policy: Do not use standard fixed reorder points
Implement dynamic reorder points recalculated monthly using rolling demand averages
Assign a dedicated demand planner exclusively for the AY segment

General Recommendations

Immediate replenishment for the 10 out-of-stock items
Urgent review and action for the 280 items currently below reorder point
Improve forecasting accuracy by collecting more historical data (minimum 2–3 years recommended)
Consider lead time variability (30–90 days) when setting safety stock and reorder points


🛠️ Tools & Technologies

Power BI (DAX for calculations and visualizations)
Data Modeling (Star Schema / Relationships on SKU_ID)
Statistical Analysis (Mean, Standard Deviation, Coefficient of Variation)
ABC-XYZ Inventory Classification Framework
Time Series Forecasting with Seasonality****
