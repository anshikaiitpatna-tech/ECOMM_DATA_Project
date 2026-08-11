
This project delivers an end-to-end analytical solution designed to evaluate sales performance, customer retention, 
profitability margins, and logistics efficiency for a global retail enterprise. By bridging relational database design
with interactive dashboard visualization, the goal is to transform raw operational data into actionable business intelligence.

Technical Stack & Architecture
Database & Querying: PostgreSQL / MySQL (Advanced SQL, CTEs, Window Functions, Database Indexing)
Data Visualization: Power BI Desktop (DAX, Dynamic Drill-Downs, Slicers, Parameter Modeling)
Data Modeling: Star Schema Architecture
ETL & Data Cleaning: Power Query / Pandas


Core Analytics Implemented
Revenue & Profit Health: Calculated net profit margins and isolated discount thresholds where margins turn negative.
Customer Segmentation (RFM): Built a 5-tier Recency, Frequency, and Monetary (RFM) model using SQL window functions
                             to classify customers into distinct cohorts (e.g., Champions, Loyal, At-Risk).
Product Pareto Analysis: Applied the 80/20 rule via running cumulative sales calculations to identify top-performing SKUs driving the majority of revenue.
Logistics & Supply Chain Operations: Tracked shipping lead times (Ship Date - Order Date) across priority tiers to identify fulfillment bottlenecks.



Business Analyst (BA) Interview & Case Study 

Question: Total revenue is increasing, but net profit margins are shrinking. How do you identify the cause?
Analysis Strategy: Group sales by category and sub-category, then cross-reference average discount percentages
against profit margins. Isolate transactions where discounts exceed 20%, as high discount rates often erode margin on low-markup items.

Question: Which shipping channels or regions are causing fulfillment delays, and how does this affect cost?

Analysis Strategy: Evaluate the gap between order date and ship date segmented by delivery mode and order priority.
Identify regions where standard shipping exceeds acceptable SLA thresholds (e.g., 5+ days) despite high shipping costs.

Question: How do you help the marketing team target high-value customers versus those at risk of churn?
Analysis Strategy: Leverage the RFM segmentation model. Filter for customers with low Recency scores but high 
Frequency and Monetary scores ("At Risk") for re-engagement campaigns, while rewarding "Champions" with loyalty programs.

Question: If management wants to reduce warehouse holding costs, how do you decide which products to keep or trim?
Analysis Strategy: Run a cumulative revenue sum using window functions to separate the catalog into the top 20% SKUs
generating 80% of revenue versus the bottom tail. Recommend liquidating or pruning slow-moving items in the bottom tier.

Question: How do you account for seasonality when evaluating sales performance?
Analysis Strategy: Compare Month-over-Month (MoM) and Year-over-Year (YoY) metrics rather than isolated monthly figures.
This accounts for predictable spikes during holiday seasons and provides a clearer baseline for year-long growth trends.
