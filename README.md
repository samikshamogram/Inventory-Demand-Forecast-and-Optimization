# Inventory-Demand-Forecast-and-Optimization
A data-driven inventory management solution using ABC classification and Prophet forecasting to analyze demand patterns. It computes key parameters like reorder point, optimal reorder quantity, and replenishment timing to improve stock control and restocking efficiency.

# Business Context
While the current dataset represents the US furniture market, this project is intended as a prototype. With deeper research into regional supply chains and Indian retail dynamics, the model can be adapted to target suitable Indian sectors for implementation, particularly in e-commerce, apparel and FMCG.

# Key Objectives
Analyze historical order and product data to understand demand patterns.
Apply ABC classification to prioritize inventory based on revenue contribution.
Use Prophet time series forecasting to predict future demand.

# Critical Inventory Control Parameters:
1. Reorder Point (ROP)
2. Reorder Quantity
3. Replenishment Timing

# Methodology
1. Data Preprocessing
Converted date fields into datetime format.
Merged product, customer, and order-level data for consolidated analysis.
Filtered invalid timestamps and ensured referential integrity across datasets.

2. ABC Classification
Computed total revenue, quantity sold, and average price per product.
Products were sorted by total revenue.
Revenue contribution was cumulatively calculated:
Class A: Top 70% revenue
Class B: Next 20%
Class C: Remaining 10%
Visualized the revenue share by ABC classes using seaborn bar plots.

3. Demand Forecasting using Prophet
For selected high-value (Class A) products, demand was aggregated daily by product ID and state.
Prophet was applied to generate demand forecasts on a per-product basis.

4. Inventory Control Metrics
Reorder Point (ROP): Based on expected demand during lead time.
Reorder Quantity: Estimated using average demand and safety stock.
Replenishment Timing: Forecasted using Prophet’s predictions and visualized to signal restocking triggers.

# Results
Products were successfully categorized into ABC classes.
Demand trends were forecasted effectively for Class A products.
Plots and CSV exports were generated to support business decision-making.

# Conclusion
This project showcases the integration of time series forecasting with classical inventory analysis to build a foundational inventory decision support tool. With further tuning, real-time data pipelines, and sector-specific adaptations, the model can be scaled for commercial use.
