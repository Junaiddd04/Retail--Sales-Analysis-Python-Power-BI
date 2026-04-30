# Retail Store Sales Analysis: End-to-End Data Analytics Project

## Project Overview
The objective of this project is to build a robust data pipeline that cleanses raw, inconsistent transactional retail data, stores it in a relational database, and delivers an interactive Power BI dashboard. The analysis covers over 13,000 retail transactions across multiple channels (Online vs. In-store) and product categories.

## Tech Stack
* **Data Cleaning & Feature Engineering**: Python (Pandas, NumPy)
* **Data Visualization (Exploratory)**: Matplotlib, Seaborn
* **Database Management**: MySQL
* **Interactive Dashboard**: Power BI

## Data Pipeline Steps

### 1. Data Cleaning (Python)
The raw dataset was processed in the Jupyter Notebook (`Data Cleaning in Python.ipynb`):
* **Column Standardization**: Converted column names to lowercase and replaced spaces with underscores.
* **Handling Missing Values**: 
    * `item`: Filled using mode based on category.
    * `price_per_unit`: Filled using median.
    * `quantity`: Filled using mode after outlier check.
* **Data Validation**: Fixed the `total_spent` column by recalculating `price * quantity`.
* **Feature Engineering**: 
    * Formatted `transaction_date` as datetime.
    * Extracted `month`, `day`, and `day_type` (Weekend/Weekday).

### 2. Database Integration (MySQL)
The cleaned data was stored in a MySQL database named `salesdb` using the `sqlalchemy` engine to enable a direct connection to Power BI.

### 3. Dashboard & Insights (Power BI)
The final interactive dashboard provides deep insights into sales performance.
<img width="1323" height="743" alt="Dashboard Image" src="https://github.com/user-attachments/assets/2842ebee-bc87-45e4-ad36-ce1d949342cd" />


#### Key Performance Indicators (KPIs)
* **Total Transactions**: 13K+
* **Total Revenue**: $1.63M
* **Total Quantity Sold**: 69.15K items
* **Average Order Value**: $129.40

#### Business Insights
* **Top Category**: Furniture leads in revenue generation.
* **Sales Timing**: 71% of sales occur on weekdays.
* **Payment Preference**: High usage of Digital Wallets for household essentials.

---
**Project by**: Mohd Junaid<br>
**LinkedIN**: www.linkedin.com/in/mohd-junaiddd04
