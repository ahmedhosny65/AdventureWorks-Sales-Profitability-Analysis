# AdventureWorks — Sales & Profitability Analysis

## Project Overview

An interactive Sales, Profitability, and Returns Analysis built in **Power BI** using the AdventureWorks dataset.

The project transforms raw transactional, customer, product, geographic, and returns data into an interactive analytical dashboard designed to monitor commercial performance, profitability, customer activity, product performance, and return behavior.

The solution provides a consolidated view of business performance and enables users to explore trends, drill into specific markets or product categories, and identify areas that require further investigation.

## Business Domain

**Retail & Sales Analytics**

The project focuses on analyzing retail sales operations across products, customers, categories, geographic markets, orders, and product returns.

Retail analytics enables organizations to understand sales performance, profitability, customer activity, product demand, geographic performance, and the financial impact of returns.

## Business Objectives

The analysis is designed to support key business questions, including:

- How is overall sales and profitability performance?
- How are revenue and orders changing over time?
- Which products and categories generate the highest sales and profit?
- Which countries and regions contribute the most revenue?
- How active are customers, and how does order activity change over time?
- Which products and categories have the highest return volumes?
- What is the return rate across different products and markets?
- What potential revenue and profit are associated with returned products?
- How reliable is the underlying data, and where do data-quality issues need attention?

## Key Performance Indicators

| KPI | Business Purpose |
|---|---|
| Revenue | Measure overall sales performance |
| Profit | Evaluate overall profitability |
| Profit Margin | Measure profitability relative to revenue |
| Orders | Monitor transaction volume |
| Active Customers | Measure customer activity |
| Average Order Value | Evaluate average revenue per order |
| Return Quantity | Monitor returned product volume |
| Return Rate | Measure the proportion of products returned |
| Lost Revenue | Estimate revenue impact from returns |
| Lost Profit | Evaluate profitability impact from returns |

## Key Results

| Metric | Value |
|---|---|
| Total Orders | 25.2K |
| Total Revenue | $24.9M |
| Total Profit | $10.5M |
| Profit Margin | 41.97% |
| Total Customers | 18K |
| Returned Orders | 1.8K |
| Return Rate | 2.17% |
| Lost Revenue from Returns | $765.3K |
| Lost Profit from Returns | $318.9K |

## Tools & Techniques

**Power BI Desktop**
Used as the primary platform for data modeling, calculation, visualization, and dashboard development.

**Power Query**
Used for data import, cleaning, transformation, and preparation across all source tables.

**Data Modeling**
Star-schema relationships connecting the Sales fact table to Products, Customers, Territories, Calendar, and Returns dimension tables.

**DAX (Data Analysis Expressions)**
Used to build measures for revenue, profit, profit margin, return rate, and lost revenue/profit calculations.

**Interactive Visuals & Slicers**
Cards, trend charts, maps, and pivot tables combined with slicers for dynamic filtering by year, category, region, and country.

**Data Validation**
Cross-checked dashboard figures against raw source files to catch data issues before drawing conclusions (see Key Insights below).

## Dataset

The analysis uses multiple AdventureWorks datasets covering different business entities:

- Sales (2015–2017)
- Customers
- Products
- Product Categories
- Product Subcategories
- Calendar
- Territories
- Returns

These datasets provide the foundation for analyzing sales transactions, customer activity, product performance, geographic distribution, and returns.

> **Note:** The 2017 sales data only covers January–June (6 months), not a full year. This is factored into the year-over-year analysis below.

## Dashboard Pages

### 1. Overview
High-level view of commercial performance across time, category, and geography.

**Key KPIs:** Orders, Revenue, Profit, Profit Margin, Customers
**Analysis:** Orders by Year · Orders by Continent/Region · Orders by Category · Category Share (Bikes/Clothing/Accessories)

**Business Questions Answered:**
- How is order volume trending over time?
- Which categories and regions generate the most orders?

### 2. Sold / Returned
Focuses on understanding sales volume alongside product return activity and its impact.

**Key KPIs:** Orders, Returns, Lost Profit, Return Rate
**Analysis:** Quantity Sold by Category/Product · Returns by Region/Country · Return Rate by Category

**Business Questions Answered:**
- Which countries and regions have the highest return volumes?
- Which categories and subcategories experience the most returns?
- What is the potential financial impact of returns?

### 3. Revenue
Detailed breakdown of profitability across category, geography, and product.

**Key KPIs:** Revenue, Profit, Profit Margin, Average Price
**Analysis:** Profit Trend by Year · Profit by Continent/Region · Profit by Category · Product-level Pivot (Category → Subcategory → Product)

**Business Questions Answered:**
- Which categories and products contribute the most profit?
- Which markets are the most profitable?
- Where is profit margin strongest, and does it align with revenue volume?

## Key Insights

- **2017 growth was initially misleading.** The dataset only covers six months of 2017, so the apparent slowdown in the year-over-year trend was not a full-year comparison. This was uncovered by validating the dashboard against the raw source files — once annualized, 2017 was outperforming 2016.
- **Bikes generated around 95% of total revenue**, showing strong performance but also a high dependency on a single category.
- **66% of customers placed only one order**, highlighting customer retention as a key growth opportunity.
- **132 products recorded zero sales** across all three years, which could indicate inactive products or a data-quality issue worth investigating.
- **Sales showed clear seasonality**, with stronger performance in the first half of the year and a decline during the summer months.

## Analysis Workflow

```
Raw AdventureWorks Data
        ↓
Data Import (Power Query)
        ↓
Data Cleaning & Transformation
        ↓
Data Modeling (Star Schema)
        ↓
DAX Measures
        ↓
Interactive Visuals
        ↓
Slicers & Filters
        ↓
Dashboard Development
        ↓
Data Validation Against Raw Source
        ↓
Business Analysis & Insights
```
