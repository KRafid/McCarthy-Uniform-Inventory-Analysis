# McCarthy-Uniform-Inventory-Analysis
Business Problem:
McCarthy Uniforms generates strong annual revenue from private school uniforms and kits; however, its inventory management system faces critical inefficiencies. A significant portion of merchandise experiences slow sales, leading to excess inventory and capital being tied up in low-performing SKUs. At the same time, high-demand items frequently go out of stock, resulting in missed sales opportunities and customer dissatisfaction.
The problem is further intensified by long supplier lead times (30–90 days), as products are manufactured overseas. This makes it difficult to respond quickly to demand fluctuations. The current inventory strategy does not effectively differentiate between high-value, fast-moving items and low-demand products, leading to both overstocking and stockouts.
Additionally, the lack of dynamic demand forecasting and adaptive reorder policies creates a mismatch between supply and actual demand patterns. As a result, the company struggles to maintain optimal inventory levels, impacting service levels, revenue potential, and operational efficiency.

Inventory Analysis Project (June 2019 – June 2020)
Overview

This project analyzes one year of inventory data on a weekly basis to understand demand patterns, stock issues, and revenue distribution across products. The main goal is to identify which products matter most and how inventory decisions can be improved.

What was done
1. Revenue and Pareto Analysis

First, I calculated:

Annual quantity
Annual revenue
Revenue share
Cumulative revenue

This was used to apply the Pareto principle (ABC analysis).

Findings:

34 items generated $291M revenue
51 items generated $85M revenue
218 items generated $42M revenue
Around 11% of products generate ~70% of revenue
2. Inventory Status
280 items (92.4%) are below reorder point
10 items (3.3%) are already out of stock

This shows a major understocking issue, especially considering lead times of 30–90 days.

3. Weekly Demand Calculation

I created a weekly table and calculated:

Weekly demand (using DAX: CALCULATE + FILTER)
Weekly sales amount (using LOOKUPVALUE)

This allowed me to track demand patterns per SKU over time.

4. Demand Variability (XYZ Analysis)

For each product, I calculated:

Average weekly demand
Standard deviation
Coefficient of variation (CV)

Then I ranked SKUs based on CV to classify them:

X → stable demand
Y → moderate variation
Z → high variation
5. ABC–XYZ Analysis

I combined revenue importance (ABC) with demand variability (XYZ).

Key observation:

High-value products include both stable and highly variable demand
Some high-revenue items are not predictable, which makes them harder to manage
6. Important Segment (AY SKUs)
AY SKUs (high value + variable demand) generate about $158.62M annually

These cannot be managed with fixed reorder points.

Suggestion:

Use dynamic reorder points
Update monthly using recent demand
These items need closer monitoring
7. Forecasting

Using weekly data (1 year) with quarterly seasonality (13 weeks):

Forecast: 251,604 units/week
Lower bound: 114,573
Upper bound: 388,635

The forecast range is wide, which shows uncertainty due to limited data (only one year).

Data Modeling
Created relationships using SKU_ID across tables
Combined stock, sales, and weekly demand data
