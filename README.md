# Customer Shopping Analytics Dashboard

An end-to-end data analytics project analyzing customer shopping behavior using Python, MySQL, and Power BI.

---

## Overview

This project explores customer shopping trends to uncover insights about purchasing behavior, seasonal patterns, customer demographics, and subscription status. The goal is to help businesses make data-driven decisions by identifying key revenue drivers and customer segments.

---

## Dataset

- **File:** `customer_shopping_data.csv`
- **Records:** 3,900 rows
- **Features:** 18 columns including Age, Gender, Category, Purchase Amount, Season, Review Rating, Subscription Status, and more.

---

## Tools & Technologies

| Tool | Purpose |
|------|---------|
| Python (Pandas) | Data loading, cleaning, EDA |
| Jupyter Notebook | Interactive analysis |
| MySQL | Data storage and SQL analysis |
| SQLAlchemy + PyMySQL | Python to MySQL connection |
| Power BI | Interactive dashboard |

---

## Project Steps

### 1. Data Loading & EDA
- Loaded dataset using Pandas
- Explored shape, data types, and summary statistics using `.info()` and `.describe()`
- Identified and handled missing values in `Review Rating` column using category-wise median imputation

### 2. Data Cleaning
- Renamed columns to snake_case for consistency
- Created new feature `age_group` using `pd.qcut()` (Young Adult, Adult, Middle-aged, Senior)
- Created `purchase_frequency_days` by mapping frequency labels to numeric values
- Dropped redundant column `promo_code_used` (found to be identical to `discount_applied`)

### 3. MySQL Integration
- Loaded cleaned DataFrame into MySQL database using SQLAlchemy
- Ran SQL queries for business analysis

### 4. Power BI Dashboard
- Connected Power BI directly to MySQL database
- Built interactive dashboard with slicers for Subscription Status, Gender, Category, and Shipping Type
- Created DAX measures for Total Revenue, Average Purchase Amount, and Customer Count

---

## Dashboard Preview

> Add a screenshot of your Power BI dashboard here

### KPIs
- Total Customers: 3.9K
- Avg Purchase Amount: $59.76
- Average Review Rating: 3.75
- Total Revenue: $233K

### Visuals
- Customer Subscription Split (Donut Chart)
- Revenue by Season (Column Chart)
- Revenue by Category (Bar Chart)
- Revenue by Age Group (Bar Chart)
- Customers by Age Group (Bar Chart)

---

## Key Findings

- Clothing is the highest revenue-generating category
- Young Adults contribute the most to overall revenue
- 73% of customers are non-subscribers, indicating a growth opportunity
- Revenue is relatively consistent across all four seasons

---

## How to Run

1. Clone this repository
2. Install dependencies:
pip install pandas sqlalchemy pymysql
3. Open `customer_shopping_eda.ipynb` in Jupyter Notebook
4. Update MySQL credentials in the connection cell:
```python
username = "your_username"
password = "your_password"
database = "your_database_name"
```
5. Run all cells
6. Open `Customer_Shopping_Analytics_Dashboard.pbix` in Power BI Desktop and refresh data

---

## Project Structure
Customer-Shopping-Analytics-Dashboard/

├── customer_shopping_data.csv

├── customer_shopping_eda.ipynb

├── customer_analysis.sql

├── Customer_Shopping_Analytics_Dashboard.pbix

├── Customer Shopping Analytics - Project Documentation.pdf

└── README.md

---

## Author

**Shantanu Shrivastava**
B.Tech CSE (AI/DS) | AKS University
[LinkedIn](https://www.linkedin.com/in/shantanushrivastava/) 
