# Walmart-Sales-Data-Analysis-Using-SQL

## Project Overview

This project focuses on analyzing Walmart’s sales data to identify high-performing branches and products, examine sales trends, and understand customer behavior. The main goal is to improve sales strategies. The dataset used comes from the Kaggle Walmart Sales Forecasting Competition.

## Project Objectives

The main aim is to gain insights from Walmart's sales data and explore the factors influencing sales across various branches.

## Data Overview

The dataset for this project was sourced from the Kaggle Walmart Sales Forecasting Competition. It includes sales transactions from three Walmart branches located in Mandalay, Yangon, and Naypyitaw. The dataset consists of 17 columns and 1,000 rows:

| Column | Description | Data Type |
| --- | --- | --- |
| `invoice_id` | Invoice number for the sale | `VARCHAR(30)` |
| `branch` | Branch where the sale occurred | `VARCHAR(5)` |
| `city` | Location of the branch | `VARCHAR(30)` |
| `customer_type` | Type of customer | `VARCHAR(30)` |
| `gender` | Gender of the customer | `VARCHAR(10)` |
| `product_line` | Product category | `VARCHAR(100)` |
| `unit_price` | Price of the product | `DECIMAL(10, 2)` |
| `quantity` | Quantity of products sold | `INT` |
| `VAT` | Tax on the purchase | `FLOAT(6, 4)` |
| `total` | Total cost of the purchase | `DECIMAL(12, 4)` |
| `date` | Date of the purchase | `DATETIME` |
| `time` | Time of the purchase | `TIME` |
| `payment` | Total amount paid | `DECIMAL(10, 2)` |
| `cogs` | Cost of goods sold | `DECIMAL(10, 2)` |
| `gross_margin_pct` | Gross margin percentage | `FLOAT(11, 9)` |
| `gross_income` | Gross income | `DECIMAL(12, 4)` |
| `rating` | Customer rating | `FLOAT(2, 1)` |

## Analysis Areas

### 1. Product Insights

Analyze the data to understand different product lines, identify top performers, and spot areas for improvement in other product lines.

### 2. Sales Insights

Examine the sales trends of various products to assess the effectiveness of sales strategies and determine areas where adjustments are needed to increase sales.

### 3. Customer Insights

Focus on identifying customer segments, understanding their buying behavior, and evaluating the profitability of each segment.

## Methodology

### 1. Data Cleaning

First, the data is cleaned by checking for any missing (NULL) values and applying appropriate strategies to handle them.

- Build a database and create a table to insert the data.
- Check for columns with NULL values (none found, as we ensured that NULL values were excluded when creating the table with `NOT NULL` constraints).

### 2. Feature Engineering

New columns will be created to provide more insights.

- **`time_of_day`**: Categorize sales into Morning, Afternoon, and Evening to analyze when most sales happen during the day.
- **`day_name`**: Extract the day of the week from the transaction date (Mon, Tue, Wed, etc.) to determine which days each branch is busiest.
- **`month_name`**: Extract the month of the year from the transaction date (Jan, Feb, Mar, etc.) to find out which months have the most sales and profit.

### 3. Exploratory Data Analysis (EDA)

Conduct an in-depth analysis to address the business questions and project objectives.

## Business Questions to Address

### 1. General Information

- How many unique cities are in the dataset?
- What city is each branch located in?

### 2. Product Insights

- How many distinct product lines exist in the dataset?
- What is the most common payment method used?
- Which product line has the highest sales?
- What is the total revenue by month?
- Which month had the highest Cost of Goods Sold (COGS)?
- Which product line generated the most revenue?
- Which city has the highest revenue?
- Which product line incurred the highest VAT?
- Label each product line as 'Good' or 'Bad' based on whether sales are above average.
- Which branch sold more than the average number of products?
- Which product line is most common by gender?
- What is the average rating for each product line?

### 3. Sales Insights

- How many sales were made by time of day and weekday?
- Which customer type generates the most revenue?
- Which city has the highest VAT (Value Added Tax)?
- Which customer type pays the most VAT?

### 4. Customer Insights

- How many unique customer types are in the data?
- How many unique payment methods are in the data?
- Which is the most common customer type?
- Which customer type makes the most purchases?
- What is the gender distribution of customers?
- What is the gender distribution across branches?
- At which time of day do customers give the most ratings?
- At which time of day do customers give the most ratings by branch?
- Which day of the week has the highest average ratings?
- Which day of the week has the highest average ratings for each branch?
