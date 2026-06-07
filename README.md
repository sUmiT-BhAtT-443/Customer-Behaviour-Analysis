# 🛒 Customer Shopping Behaviour Analysis

An end-to-end Data Analytics project focused on understanding customer purchasing behavior, identifying revenue drivers, analyzing customer segments, and generating actionable business insights using Python, SQL Server, and Power BI.

---

## 📌 Project Overview

Organizations generate large volumes of customer transaction data every day, but raw data alone cannot support strategic decision-making.

This project demonstrates a complete analytics workflow:

- Data Cleaning & Preprocessing using Python
- Data Storage and Querying using SQL Server
- Business Insight Generation using SQL
- Interactive Dashboard Development using Power BI

The project helps answer critical business questions such as:

- Which product categories generate the highest revenue?
- Do discounts actually increase purchase value?
- Which customer segments contribute the most revenue?
- Are subscription customers more valuable?
- Which products perform best and worst?
- Which locations drive the highest sales?

---

## 🎯 Business Objectives

- Understand customer purchasing behavior
- Identify top-performing product categories
- Evaluate discount effectiveness
- Analyze customer demographics
- Compare subscription vs non-subscription customers
- Identify best and worst performing products
- Support data-driven business decisions

---

## 🛠️ Technology Stack

| Technology | Purpose |
|------------|----------|
| Python | Data Cleaning & Transformation |
| Pandas | Data Analysis |
| SQL Server | Data Storage |
| SQL | Business Insights |
| SQLAlchemy | Database Connectivity |
| Power BI | Dashboard & Visualization |
| Git & GitHub | Version Control |

---

## 📂 Dataset Information

### Dataset Summary

| Metric | Value |
|----------|---------|
| Original Records | 5,050 |
| Duplicate Records Removed | 50 |
| Final Records | 5,000 |
| Features | 17 |

### Features

- Customer ID
- Age
- Gender
- Item Purchased
- Category
- Purchase Amount
- Location
- Size
- Color
- Season
- Review Rating
- Subscription Status
- Shipping Type
- Discount Applied
- Previous Purchases
- Payment Method
- Frequency of Purchases

---

# 🔄 Project Workflow

```text
Raw Dataset
     │
     ▼
Data Understanding
     │
     ▼
Data Cleaning
     │
     ▼
Missing Value Treatment
     │
     ▼
Category Standardization
     │
     ▼
Duplicate Removal
     │
     ▼
SQL Server Integration
     │
     ▼
Business Insight Queries
     │
     ▼
Power BI Dashboard
     │
     ▼
Business Recommendations
```

---

# 🧹 Data Cleaning & Preprocessing

Several preprocessing steps were performed to improve data quality and consistency.

## 1. Category Validation & Correction

The original dataset contained incorrect mappings between products and categories.

Examples:

| Product | Correct Category |
|----------|----------|
| Laptop | Electronics |
| Phone | Electronics |
| Shoes | Footwear |
| Backpack | Accessories |
| Jacket | Outerwear |

A custom mapping dictionary was created and applied to standardize category assignments.

---

## 2. Missing Value Treatment

### Size Column

Handled based on product category:

| Category | Treatment |
|-----------|------------|
| Electronics | Not Applicable |
| Accessories | Free Size |
| Footwear | Not Available |
| Clothing | Filled with Mode |

---

### Review Rating

Missing ratings were replaced using:

```python
Mean Rating of Same Product
```

This preserved product-specific rating behavior.

---

### Previous Purchases

Missing values replaced with:

```python
0
```

---

### Purchase Amount

Missing purchase values were imputed using:

```python
Average Purchase Amount of Same Product
```

---

## 3. Duplicate Removal

Duplicate customer records were identified and removed.

### Before Cleaning

```text
5050 Rows
```

### After Cleaning

```text
5000 Rows
```

---

## 4. Column Standardization

Column names were standardized:

### Example

```text
Purchase Amount (USD)
```

Converted to:

```text
purchase_amount
```

All columns were converted to lowercase and snake_case format.

---

# 🗄 SQL Server Integration

The cleaned dataset was loaded into SQL Server using SQLAlchemy.

### Database

```sql
customer_behavior_analysis
```

### Table

```sql
customer_behavior_analysis
```

### Connection Technologies

- pyodbc
- SQLAlchemy
- SQL Server Express

---

# 📊 Power BI Dashboard

The project contains two interactive dashboard pages.

---

# Dashboard 1: Customer Revenue Analysis

![Customer Revenue Analysis](https://i.postimg.cc/tC6RS2pv/revenue-analysis.png)

### KPIs

- Total Customers
- Unique Items
- Average Review Rating
- Total Revenue
- Average Spend

### Analysis Performed

- Revenue by Gender
- Revenue by Category
- Revenue by Season
- Revenue by Payment Method
- Revenue by Age Distribution
- Customer Count & Revenue by Location
- Shipping Type Analysis

### Interactive Filters

- Category
- Gender
- Subscription Status
- Discount Applied

---

# Dashboard 2: Best vs Worst Analysis

![Best vs Worst Analysis](https://i.postimg.cc/Dzrb97hC/Best-Worst.png)

### Top Performance Analysis

- Top 5 Products by Rating
- Top 5 Products by Revenue
- Top 5 Locations by Revenue

### Bottom Performance Analysis

- Bottom 5 Products by Rating
- Bottom 5 Products by Revenue
- Bottom 5 Locations by Revenue

---

# 🔍 SQL Business Insights

A set of business-focused SQL queries were developed to answer real-world business questions.

---

## 1. Which Category Generates the Highest Revenue?

Purpose:

- Identify revenue-driving categories
- Support inventory planning
- Improve marketing investment decisions

---

## 2. Are Discounts Increasing Purchase Value?

Purpose:

- Measure discount effectiveness
- Reduce unnecessary discount spending
- Improve profitability

---

## 3. Revenue Contribution by Gender

Purpose:

- Understand customer segments
- Enable targeted marketing campaigns
- Improve personalization

---

## 4. High-Spending Discount Customers

Purpose:

- Identify premium customers using discounts
- Create targeted promotional campaigns

---

## 5. Top & Bottom Rated Products

Purpose:

- Improve product quality
- Promote highly rated products
- Increase customer satisfaction

---

## 6. Shipping Type Analysis

Purpose:

- Compare customer spending across shipping methods
- Optimize shipping strategy

---

## 7. Subscription Customer Analysis

Purpose:

- Measure effectiveness of subscription programs
- Improve customer loyalty initiatives

---

## 8. Products with Highest Discount Dependency

Purpose:

- Identify products heavily dependent on discounts
- Improve pricing strategies

---

## 9. Customer Segmentation

Customers segmented into:

- New Customers
- Returning Customers
- Loyal Customers

Purpose:

- Improve retention strategy
- Personalize marketing efforts

---

## 10. Top 3 Products Within Each Category

Purpose:

- Improve recommendations
- Optimize inventory management
- Increase sales through best-selling products

---

## 11. Repeat Buyer vs Subscription Analysis

Purpose:

- Understand relationship between customer loyalty and subscriptions
- Improve subscription targeting

---

## 12. Revenue Contribution by Age Group

Age Groups:

- 18–25
- 26–35
- 36–50
- 51+

Purpose:

- Enable demographic-based marketing
- Improve customer targeting

---

# 💡 Key Findings

### Electronics Category Generates the Highest Revenue

Electronics products contribute significantly to overall revenue compared to other categories.

---

### Subscription Customers Show Strong Spending Behavior

Subscription users contribute substantial revenue and represent an important customer segment.

---

### Major Cities Drive Revenue

Locations such as:

- New York
- Los Angeles
- Chicago

generate significant sales volume.

---

### Product Ratings Influence Performance

Highly rated products consistently outperform lower-rated products in revenue generation.

---

### Revenue Distribution Varies Across Age Groups

Different age segments contribute differently to revenue, enabling targeted marketing opportunities.

---

# 📈 Business Recommendations

### Product Strategy

- Focus inventory on high-performing categories
- Promote top-rated products

### Customer Strategy

- Expand subscription programs
- Reward loyal customers

### Marketing Strategy

- Build demographic-specific campaigns
- Target high-revenue customer segments

### Pricing Strategy

- Evaluate discount dependency
- Reduce unnecessary promotional spending

### Geographic Strategy

- Invest more in high-performing locations
- Improve performance in underperforming regions

---

# 📁 Project Structure

```text
Customer-Shopping-Behaviour-Analysis
│
├── Dataset
│   └── customer_shopping_behavior.csv
│
├── Notebook
│   └── Analysis.ipynb
│
├── SQL
│   └── Business_Insights.sql
│
├── PowerBI
│   └── Customer_Behaviour_Analysis.pbix
│
├── Dashboard_Images
│   ├── Customer_Revenue_Analysis.png
│   └── Best-Worst.png
│
├── README.md
│
└── requirements.txt
```

---

# 🚀 How to Run

### Clone Repository

```bash
git clone https://github.com/yourusername/customer-shopping-behaviour-analysis.git
```

### Navigate

```bash
cd customer-shopping-behaviour-analysis
```

### Install Dependencies

```bash
pip install pandas sqlalchemy pyodbc
```

### Open

- Analysis.ipynb
- Business_Insights.sql
- Customer_Behaviour_Analysis.pbix

---

# 👨‍💻 Author

### Sumit Bhatt

Data Analytics Enthusiast

Skills:

- Python
- SQL
- Power BI
- Data Cleaning
- Data Visualization
- Business Analytics

---

⭐ If you found this project useful, consider giving it a star.
