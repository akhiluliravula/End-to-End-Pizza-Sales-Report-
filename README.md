# End-to-End-Pizza-Sales-Report-
Here is a complete, clear, and structured topic-by-topic breakdown of the End to End Pizza Sales Report Project using Microsoft Power BI.


1. Project Overview & Business Objective
Goal:
* Analyze historical pizza sales data to identify revenue trends, order patterns, customer preferences, and sales metrics to help management optimize operations and inventory.

* Primary Analytics Focus: Tracking high-level KPIs, identifying busy hours/days, and analyzing product performance (Top and Bottom Sellers).

  
2. Dataset & Data Structure
The dataset represents order transactions and product metadata over a specific period (typically ~48,000+ transaction rows).

Key Data Fields:

order_id: Unique ID for each order.

pizza_id: Identifier for individual pizzas sold.

quantity: Number of units ordered per row.

order_date & order_time: Timestamp of the transaction.

unit_price & total_price: Pricing details for single units and calculated order totals.

pizza_size: Categorical sizing (S, M, L, XL, XXL).

pizza_category: Product categories (Classic, Veggie, Supreme, Chicken).

pizza_name: Specific pizza variants (e.g., Thai Chicken Pizza, The Brie Carre Pizza).



3. Key Performance Indicators (KPIs) & DAX Measures
 The dashboard relies on custom Data Analysis Expressions (DAX)to calculate essential business metrics:
1 Total Revenue: Total sales generated from all orders.$$\text{Total Revenue} = \sum(\text{total\_price})$$
2.Average Order Value (AOV): Average dollar amount spent per order.$$\text{AOV} = \frac{\text{Total Revenue}}{\text{Total Orders}}$$
3.Total Pizzas Sold: Cumulative quantity of pizzas ordered.$$\text{Total Quantity} = \sum(\text{quantity})$$
4.Total Orders: Count of unique orders.$$\text{Total Orders} = \text{DISTINCTCOUNT}(\text{order\_id}) \quad \text{}$$
5.Average Pizzas Per Order: Average number of pizzas included in a single order.$$\text{Average Pizzas per Order} = \frac{\text{Total Quantity}}{\text{Total Orders}}$$



4. Dashboard Architecture & Visual Analysis
Page 1: Home / Executive Summary
KPI Card Visuals: Quick single-value displays for Revenue, Total Orders, Average Order Value, and Total Quantity.

Daily Trend for Total Orders: Bar/Column chart showing peaks across days of the week (identifies Friday/Saturday evening peaks).

Monthly Trend for Total Orders: Line chart demonstrating seasonality and volume trends over time.

Percentage of Sales by Category: Donut/Pie chart highlighting revenue contributions from Classic, Veggie, Supreme, and Chicken pizzas.

Percentage of Sales by Size: Breakdown comparing Small, Medium, Large, and Extra-Large pizza popularity.

Page 2: Detailed Performance & Top/Bottom Sellers
Top 5 Pizzas: Bar chart identifying the highest-performing pizzas based on Revenue, Quantity, and Total Orders.

Bottom 5 Pizzas: Bar chart highlighting the worst-performing products (e.g., Brie Carre Pizza) to support menu consolidation or promotion efforts.

Interactive Slicers: Date range selectors, pizza category filters, and size filters to drill down into specific customer segments.






5. Technical Implementation Steps
Data Cleaning & Transformation (Power Query):

Corrected data types for dates, times, unit prices, and quantities.

Created custom columns for Day Name, Month Name, and Order Hour to enable time-series analysis.

Handled missing values or formatting inconsistencies.

Data Modeling:

Structured data using proper primary keys (order_id, pizza_id).

Formed dynamic relationships using a dedicated Calendar Dimension Table (dim_date) for time-intelligence functions.

UI/UX Optimization:

Used consistent color themes, structured container layouts, clear visual alignment, and navigation buttons for switching dashboard pages.
