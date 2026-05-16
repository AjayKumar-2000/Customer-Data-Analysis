# Customer Shopping Behavior Analysis 🛍️📊

An end-to-end data analytics project that explores customer spending patterns, segments shopper demographics, and evaluates purchasing behaviors using **Python**, **SQL (MySQL)**, and **Power BI**. The project transforms raw transactional data into actionable strategic recommendations to optimize business growth and subscription models.

---

## 🚀 Project Overview
This repository contains a full data analytics pipeline based on a dataset of **3,900 consumer purchases** spanning **18 distinct behavioral and demographic features**. The primary objective is to evaluate transactional metrics (average spends, product ratings, categories) and identify key target markets to drive revenue optimizations.

### Key Metrics At a Glance
* **Total Transactions Analyzed:** 3,900 Purchases
* **Average Order Value (AOV):** $59.76
* **Average Product Review Rating:** 3.75 / 5.0
* **Customer Subscriptions:** 27% Subscribed | 73% Non-Subscribers

---

## 🛠️ Tech Stack & Tools Used
* **Data Preparation & Feature Engineering:** Python (Pandas, NumPy)
* **Database Storage & Structured Querying:** SQL (MySQL Server)
* **Data Visualization & Interactive Dashboarding:** Power BI Desktop

---

## 🔄 Data Pipeline Architecture

### 1. Data Preparation (Python)
The initial ETL (Extract, Transform, Load) phase was handled in a Python environment using Jupyter Notebooks:
* **Exploration:** Conducted structural evaluations using `df.info()` and statistical summaries via `df.describe()`.
* **Data Imputation:** Imputed 37 missing values in the `Review Rating` column using the median rating score of their corresponding product categories.
* **Column Standardization:** Transformed column headers into clean, uniform `snake_case` naming conventions.
* **Feature Engineering:** * Binned continuous customer ages into a categorical `age_group` column.
    * Synthesized a `purchase_frequency_days` field to measure time elapsed between purchases.
* **Database Integration:** Dropped redundant attributes (such as `promo_code_used`) and pushed the cleaned dataframe directly into a localized MySQL database via `sqlalchemy`.

### 2. Relational Database Analysis (MySQL)
Once stored in MySQL, complex queries were executed to extract deep analytical business insights:
* **Demographic Performance:** Measured total revenue generated across distinct genders.
* **Loyalty & Value Tracking:** Segmented shoppers who leveraged discounts yet still maintained a final checkout value above the platform's standard average purchase amount.
* **Product Performance Matrix:** Isolated top 5 highest-rated products and calculated discount dependencies across inventory categories.
* **RFM Customer Segmentation:** Classified customer profiles into **New**, **Returning**, and **Loyal** segments based on total historical purchase volume.

### 3. Business Intelligence Dashboard (Power BI)
Built an interactive dashboard allowing stakeholders to slice metrics dynamically by:
* Subscription Status (`Yes` / `No`)
* Gender Profile (`Male` / `Female`)
* Product Category (`Clothing`, `Accessories`, `Footwear`, `Outerwear`)
* Shipping Methodology (`Standard`, `Express`, `2-Day Shipping`, etc.)

---

## 📈 Key Analytical Findings

* **Gender Spend Divergence:** Male customers act as a core engine, generating roughly **2× more revenue** ($157.8K) compared to female customers ($75.2K).
* **The Subscription Opportunity:** Non-subscribers account for **73% of the total customer volume** and **73% of total aggregate revenue ($170,436)**. Interestingly, a vast majority of highly active repeat buyers (those with >5 historical orders) remain entirely unsubscribed, flagging a massive conversion opportunity.
* **Product Dominance:** The **Clothing** category significantly leads performance metrics across all quadrants, with **Young Adults** contributing the highest relative share of revenue.
* **Shipping & Spend Correlation:** Customers opting for Express Shipping demonstrate a higher baseline spending average ($60.48) than those selecting Standard Shipping ($58.46).

---

## 💡 Strategic Business Recommendations

1. **Maximize Subscription Conversions:** Launch targeted email marketing tracks specifically offering onboarding incentives to the 73% non-subscriber segment, positioning it as a value-adder for repeat buyers.
2. **Optimize Discount Guardrails:** Products like *Hats* (50% discount rate) and *Sneakers* (49.66% discount rate) show highly discount-dependent behavior. Review pricing structures to protect net margins.
3. **Loyalty Program Rollouts:** Implement structured milestone tiers to incentivize "Returning" shoppers into migrating permanently into the highly profitable "Loyal" tier.
4. **Targeted ROI Campaigns:** Focus primary marketing spends on **Young Adults** and premium **Express Shipping** cohorts to maximize immediate conversion values.

---

## 📁 Repository Structure
```text
├── data/
│   ├── raw_shopping_behavior.csv       # Original dataset
│   └── cleaned_shopping_data.csv       # Processed dataset output from Python
├── python/
│   └── data_cleaning_etl.ipynb         # Python Pandas data prep notebook
├── sql/
│   └── business_queries.sql            # MySQL analytical query scripts
├── dashboard/
│   └── customer_behavior_db.pbix       # Power BI Dashboard file
└── README.md
