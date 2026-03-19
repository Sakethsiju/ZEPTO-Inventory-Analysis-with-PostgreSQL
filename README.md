# Zepto Inventory Analysis with PostgreSQL

**Tools:** PostgreSQL · SQL  
**Dataset:** Zepto product inventory (Kaggle)  
**Domain:** Retail Analytics · Inventory Management · Business Intelligence

---

## 📌 Project Overview

This project analyzes a **Zepto quick-commerce inventory dataset** using PostgreSQL to extract actionable insights on product performance, pricing strategy, revenue contribution, and logistics planning. Every query is designed to answer a real business question faced by inventory and operations teams.

---

## 🎯 Business Problems Solved

| # | Business Question | Finding |
|---|---|---|
| 1 | Which products offer the best value to customers? | Top 10 highest-discount products identified across categories |
| 2 | Which high-value products are out of stock? | High-MRP products with `outOfStock = TRUE` — direct revenue loss |
| 3 | Which categories drive the most revenue? | Revenue contribution ranked by category using SUM of selling price × quantity |
| 4 | How heavy is the inventory by category? | Total weight calculated for logistics and storage planning |

---

## 🔍 Key Findings

### 1. Best-Value Products (Top 10 Discounts)
- Filtered and ranked products by `discountPercent` in descending order
- Highest discounts applied across a wide variety — from snacks to food essentials
- Insight: Discount strategy is broad, not category-specific — suggesting customer acquisition focus over margin optimization

### 2. High-MRP Out-of-Stock Products
- Filtered products where `outOfStock = TRUE` and `mrp` exceeds a high-value threshold
- Identified high-demand, high-value items unavailable to customers
- Insight: These represent direct missed revenue — restocking priority list delivered to management

### 3. Revenue by Category
- Used `SUM(discountedSellingPrice × availableQuantity)` grouped by category
- Top revenue contributors: Munchies, Cooking Essentials
- Insight: High-revenue categories should receive priority in stock replenishment planning

### 4. Inventory Weight & Logistics
- Calculated `SUM(weightInGms × availableQuantity)` grouped by category
- Lightest: Meats, Fish & Eggs (fast turnover, limited shelf life)
- Heaviest: Munchies (large stable stock)
- Insight: Weight distribution directly informs warehouse layout and delivery route planning

---

## 🛠️ Tools & Techniques

| Tool | Usage |
|---|---|
| **PostgreSQL** | Table creation, data import, SQL querying, aggregation |
| **SQL** | Filtering, GROUP BY, ORDER BY, SUM, COUNT, subqueries |
| **Kaggle** | Dataset source |

---

## 📁 Project Files

```
ZEPTO-Inventory-Analysis-with-PostgreSQL/
│
├── ZEPTO(DATASET).csv              # Raw inventory dataset
├── ZEPTO(QUERIES).sql              # All SQL queries used for analysis
├── ZEPTO(INSIGHTS Q&A).pdf         # Key findings and business insights
│
└── README.md
```

## 💡 Business Recommendations

| Area | Recommendation |
|---|---|
| Out-of-stock items | Immediate restocking of high-MRP products to prevent revenue loss |
| Discount strategy | Narrow discounts to underperforming categories instead of broad application |
| Category investment | Double down on Munchies and Cooking Essentials — highest revenue contributors |
| Logistics planning | Prioritize warehouse space for heaviest categories based on weight analysis |

---

## 🚀 How to Run This Project

1. Clone the repo:
   ```bash
   git clone https://github.com/Sakethsiju/ZEPTO-Inventory-Analysis-with-PostgreSQL.git
   ```
2. Set up PostgreSQL on your system
3. Open `ZEPTO(QUERIES).sql` — run the `CREATE TABLE` statement first
4. Import `ZEPTO(DATASET).csv` into the `zepto` table
5. Run each query section by section
6. Open `ZEPTO(INSIGHTS Q&A).pdf` to view pre-computed findings

---

## 📫 Connect with Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/enugu-saketh-reddy-21k91a6631)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:sakethsiju63@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Sakethsiju)

---

*Part of my Data Analyst portfolio — using SQL to solve real inventory and operations problems.*
