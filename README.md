# 🍕 Food Delivery Cost & Profitability Analysis


## 🎯 Project Goals
- Clean and preprocess raw delivery order data  
- Perform exploratory analysis to identify patterns  
- Calculate profit and cost metrics  
- Present insights that can help with pricing or operational decisions

---

## 📁 Dataset
- **Source:** Public dataset (mention source or URL if available)  
- **Primary File:** `data.csv` (or actual name)  
- **Content:** Delivery orders with cost, delivery time, and price metrics

---

## Problem Statement
The objective of this project was to analyze the cost and revenue structure of a food delivery business to determine overall profitability and identify key factors affecting profit per order. The goal was to understand whether the current pricing and discount strategy was sustainable and to recommend changes to improve profitability.

---

## Dataset
The dataset contains order-level data for a food delivery platform, including:
Order value
Delivery fee
Discount amount
Commission fee
Payment processing fee
Delivery time
City
Order date
Each row represents a single order, and profitability is calculated as:
Profit = Commission Fee − (Delivery Cost + Discount + Payment Processing Fee)

---

## Analysis Performed
The following analyses were performed:
Cost vs Revenue analysis
Profit per order calculation
Profit distribution analysis
Profitability by city
Profitability by discount range
Profitability by delivery time
Profitability by order value
Scenario simulation to test different commission and discount strategies
Python (Pandas) was used for data cleaning and analysis, and Matplotlib/Seaborn were used for visualization.

---

## Key Insights
(You should adjust based on your results, but here is a strong example)
A large percentage of orders were not profitable, mainly due to high discount values.
Orders with high discounts (> 30%) were mostly loss-making.
Orders with higher order value were more likely to be profitable.
Some cities were consistently profitable, while others had high delivery costs leading to losses.
Long delivery times increased delivery cost, which reduced profitability.
The current commission structure was not sufficient to cover delivery and discount costs in many cases.

---

## Recommendations
Based on the analysis:
Reduce discounts on low-value orders.
Increase commission percentage for high-discount orders.
Introduce a minimum order value for discounts.
Optimize delivery routes to reduce delivery costs for long-distance orders.
Focus marketing and promotions on high-value orders, which are more profitable.
Adjust pricing strategy city-wise based on delivery cost and profitability.

---

## Business Impact
If the recommended changes are implemented:
The company can reduce loss-making orders.
Profit margin per order can be increased.
Discount strategy can be optimized to balance customer acquisition and profitability.
Operational costs can be reduced through delivery optimization.
Overall business sustainability and profitability will improve.

---

## SQL Analysis Section 

Columns:
order_id
city
order_value
delivery_fee
discount
commission
payment_fee
delivery_time
profit

## Top 10 Cities by Profit
SELECT city,
       SUM(profit) AS total_profit
FROM orders
GROUP BY city
ORDER BY total_profit DESC
LIMIT 10;

---

## Average Profit Per Order
SELECT AVG(profit) AS avg_profit_per_order
FROM orders;

---

## Profit by Discount Range
SELECT 
    CASE 
        WHEN discount = 0 THEN 'No Discount'
        WHEN discount BETWEEN 1 AND 50 THEN 'Low Discount'
        WHEN discount BETWEEN 51 AND 100 THEN 'Medium Discount'
        ELSE 'High Discount'
    END AS discount_range,
    AVG(profit) AS avg_profit
FROM orders
GROUP BY discount_range
ORDER BY avg_profit DESC;

---

## Profit by Delivery Time
SELECT 
    CASE 
        WHEN delivery_time < 20 THEN 'Fast Delivery'
        WHEN delivery_time BETWEEN 20 AND 40 THEN 'Medium Delivery'
        ELSE 'Slow Delivery'
    END AS delivery_speed,
    AVG(profit) AS avg_profit
FROM orders
GROUP BY delivery_speed
ORDER BY avg_profit DESC;

---

## Profit by Order Value
SELECT 
    CASE 
        WHEN order_value < 200 THEN 'Low Value'
        WHEN order_value BETWEEN 200 AND 500 THEN 'Medium Value'
        ELSE 'High Value'
    END AS order_value_range,
    AVG(profit) AS avg_profit
FROM orders
GROUP BY order_value_range
ORDER BY avg_profit DESC;


## 📊 How to Run This Project
1. Clone this repository:
   ```bash
   git clone https://github.com/R1SH48/Food-delivery-cost-and-profitability.git
