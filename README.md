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

## 🛠 Technologies Used
| Language / Tool | Purpose |
|----------------|---------|
| Python         | Data processing & analysis |
| Pandas         | Data cleaning & manipulation |
| Numpy          | Numerical operations |
| Matplotlib / Seaborn | Visualization |
| Jupyter Notebook | Interactive analysis |

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

## 📊 How to Run This Project
1. Clone this repository:
   ```bash
   git clone https://github.com/R1SH48/Food-delivery-cost-and-profitability.git
