Customer Shopping Behavior Analysis
Project Overview

This project analyzes customer shopping behavior using transactional retail data to uncover insights into customer spending patterns, product preferences, subscription behavior, and customer segments.

The analysis combines:

Python for data cleaning and preprocessing
MySQL for business-focused analytical queries
Power BI for interactive dashboard visualization

The goal is to transform raw transactional data into actionable business insights that can support strategic decision-making.

Dataset Information

The dataset contains information from 3,900 customer purchases across multiple product categories.

Features Included
Customer demographics
Age
Gender
Location
Subscription Status
Purchase details
Item Purchased
Category
Purchase Amount
Season
Size
Color
Shopping behavior
Discount Applied
Previous Purchases
Purchase Frequency
Review Rating
Shipping Type
Technologies Used
Tool / Technology	Purpose
Python	Data cleaning & preprocessing
Pandas	Data manipulation
MySQL	Business query analysis
Power BI	Dashboard & visualization
Excel	Initial dataset handling
Project Workflow
1. Data Preparation in Python
Tasks Performed
Loaded dataset using Pandas
Performed exploratory data analysis using:
df.info()
df.describe()
Checked and handled missing values
Standardized column names into snake_case
Created new engineered features
Missing Value Handling

The review_rating column contained 37 missing values.

These missing values were imputed using:

Median review rating of each product category
Feature Engineering

Created:

age_group
purchase_frequency_days
Data Consistency Validation
Verified redundancy between:
discount_applied
promo_code_used
Removed unnecessary duplicate information
SQL Integration

The cleaned dataset was loaded into MySQL for structured business analysis.

SQL Business Analysis

The project answers multiple business-oriented analytical questions using SQL.

Key Analyses Performed
Revenue Analysis
Revenue by gender
Revenue by age group
Revenue by subscription status
Customer Behavior Analysis
Repeat buyers vs subscription behavior
High-spending discount users
Customer segmentation:
New
Returning
Loyal
Product Analysis
Top 5 highest-rated products
Top products per category
Discount-dependent products
Shipping Analysis
Comparison between:
Standard shipping
Express shipping
Key Insights
Revenue & Spending
Male customers generated nearly 2× more revenue than female customers.
Express shipping users spent slightly more on average compared to standard shipping users.
839 customers used discounts while still spending above the average purchase amount.
Customer Segmentation

Customers were segmented based on purchase history into:

New Customers
Returning Customers
Loyal Customers

Analysis showed:

Loyal customers dominate repeat purchases
Many repeat buyers are still not subscribed
Subscription Insights
Non-subscribers represented:
73% of customers
73% of total revenue

This indicates a strong opportunity for subscription conversion strategies.

Product Insights
Highest Rated Products
Gloves
Sandals
Boots
Hat
Skirt
Most Discount-Dependent Products
Hat
Sneakers
Coat
Sweater
Pants
Power BI Dashboard

An interactive Power BI dashboard was developed to visualize:

Revenue trends
Customer segments
Product performance
Subscription analysis
Shipping behavior
Dashboard Filters
Subscription Status
Gender
Category
Shipping Type
Business Recommendations
Increase Subscription Conversion

Provide exclusive subscriber benefits to convert non-subscribers.

Customer Loyalty Programs

Reward repeat buyers to move more customers into the loyal segment.

Optimize Discount Strategy

Balance discount campaigns with profitability for highly discounted products.

Targeted Marketing

Focus marketing campaigns on:

Young adults
Express shipping users
High-spending customer groups
Skills Demonstrated
Data Cleaning
Exploratory Data Analysis (EDA)
Feature Engineering
SQL Query Writing
Business Intelligence
Dashboard Development
Data Visualization
Analytical Thinking
Project Structure
Customer-Shopping-Behavior-Analysis/
│
├── data/
├── python/
├── sql/
├── powerbi/
├── presentation/
├── report/
└── README.md
Future Improvements
Add predictive analytics models
Customer churn prediction
Recommendation system
Sales forecasting
Automated ETL pipeline
Author

Ajay
Master’s Student in Information Technology at TH OWL
Skills: Python, SQL, Power BI, Excel, Data Analytics & Machine Learning
