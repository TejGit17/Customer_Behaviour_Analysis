# Customer_Behaviour_Analysis
Business analytics project showcasing customer behavior analytics using Python, SQL, Power BI.
Customer Behavior Analysis — Data Analytics Project
Overview

This project analyzes customer purchasing behavior to uncover insights around spending patterns, discounts, subscriptions, and product performance. The workflow covers the full analytics pipeline — from raw data ingestion in Python, to SQL-based analysis in PostgreSQL, to an interactive Power BI dashboard, and a final summary report and presentation.

The goal is to answer key business questions such as:

How does revenue differ across customer segments (e.g., gender, subscription status)?
Which customers respond to discounts, and does it drive spend?
What are the top-performing products by rating and order volume?
Are repeat buyers more likely to subscribe?
Dataset
Source: Customer transaction dataset (CSV)
Storage: Loaded into a PostgreSQL database (customer_behavior) using Python
Key columns:
customer_id, gender, previous_purchases
item_purchased, category, purchase_amount
discount_applied, subscription_status
review_rating
Tools & Technologies
Category	Tools
Data Loading & Cleaning	Python (pandas, SQLAlchemy)
Database	PostgreSQL
Querying & Analysis	SQL (aggregations, CTEs, window functions)
Visualization	Power BI
Reporting	Word / PDF summary report
Presentation	Gamma (AI-generated PPT)
Steps
1. Data Loading (Python)
Loaded the raw dataset into a pandas DataFrame
Connected to PostgreSQL using SQLAlchemy and psycopg2
Wrote the cleaned DataFrame into a SQL table using to_sql()
2. Exploratory Data Analysis (EDA)
Inspected data types, missing values, and distributions in Python
Identified key categorical and numerical fields for further analysis
3. Data Cleaning
Standardized column values (e.g., consistent casing for discount_applied, subscription_status)
Verified data types (ensured numeric fields like purchase_amount weren't stored as text)
Handled duplicate and inconsistent entries
4. SQL Analysis

Performed analysis directly in PostgreSQL using queries such as:

Revenue breakdown by gender
Customers who used discounts but still spent above average
Top 5 products by average review rating
Discount rate by product category
Customer segmentation (New / Returning / Loyal) based on purchase history
Top 3 best-selling items per category using window functions
Subscription likelihood among repeat buyers
5. Power BI Dashboard
Connected Power BI directly to the PostgreSQL database
Built interactive visuals including KPI cards, category breakdowns, and trend charts
Used filters and slicers to explore customer segments dynamically
6. Reporting
Summarized key findings and business recommendations in a written report
Highlighted actionable insights for marketing and inventory decisions
7. Presentation
Created a concise, visual presentation using Gamma to communicate findings to a non-technical audience
Dashboard

(Add a screenshot or link to your published Power BI dashboard here)

Example:

![Dashboard Preview](dashboard_screenshot.png)
Results
Identified customer segments with the highest revenue contribution
Found that discount usage does not always correlate with lower average spend
Surfaced top-performing products by both sales volume and customer satisfaction
Established a clear link between purchase frequency and subscription likelihood

(Replace with your specific findings once analysis is finalized)

How to Run
Prerequisites
Python 3.x with pandas, sqlalchemy, psycopg2-binary
PostgreSQL installed and running
Power BI Desktop
Steps
Clone this repository
bash
   git clone <repo-url>
Install Python dependencies
bash
   pip install pandas sqlalchemy psycopg2-binary
Update database credentials in load_data.py
Run the data loading script
bash
   python load_data.py
Open PostgreSQL and run the SQL scripts in /sql to reproduce the analysis
Open dashboard.pbix in Power BI Desktop and connect it to your local PostgreSQL instance
Refresh the dataset to view the latest data
Project Structure
├── data/
│   └── customer_data.csv
├── sql/
│   └── analysis_queries.sql
├── load_data.py
├── dashboard.pbix
├── report.pdf
└── README.md
Author

(Tejus R,
Linkedin:www.linkedin.com/in/tejus-r-836842272)
