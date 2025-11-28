# KPMG Customer & Sales Data Analysis

This project is an end-to-end **customer and sales data analysis** case study based on the **KPMG virtual internship dataset**.  
Using **Microsoft Excel** (formulas, pivot tables, charts, basic modeling), I cleaned and analyzed multiple related tables to generate **actionable insights** on customers, transactions, new-customer potential, and **Customer Lifetime Value (CLV)**.

> ✅ Built for **Data Analyst / Business Analyst** roles  
> ✅ Uses ATS-friendly keywords: *data cleaning, data transformation, customer segmentation, transaction analysis, CLV, Excel, dashboards, KPI reporting, revenue analysis*.

---

## 📂 Dataset Overview

Main sheets used from `KPMG final project.xlsx`:

- **`customer_demographic`** – **4,000 rows × 13 columns**  
  Customer details: gender, DOB, job_title, job_industry_category, wealth_segment, tenure, etc.

- **`customer_address`** – **3,999 rows × 6 columns**  
  Address-level details: state, postcode, country, property_valuation.

- **`transactions`** – **19,445 rows × 13 columns**  
  Transaction data: transaction_id, product_id, customer_id, transaction_date, online_order, list_price, standard_cost, brand, product_line, etc.

- **`new_customer_list`** – **1,000 rows × 23 columns**  
  New/prospect customers with demographic and address information.

🔢 **Total volume processed:**  
~**28,000+ records** across customers and transactions.

---

## 🛠 Tech Stack & Skills (ATS-Friendly)

- **Tools:**  
  - Microsoft Excel (formulas, conditional formatting, data validation)  
  - Pivot Tables & Pivot Charts  
  - Basic Excel-based modeling for **CLV** and segmentation  

- **Core skills demonstrated:**  
  - Data Cleaning & Data Quality  
  - Data Transformation & Table Joining (via `customer_id`)  
  - Customer Segmentation (wealth segment, industry, geography)  
  - Transaction & Revenue Analysis  
  - Customer Lifetime Value (CLV) Calculation  
  - Dashboard-style summaries & KPI reporting  
  - Business Storytelling / Executive Summary

---

## 🔍 Project Tasks & Logic

### 1️⃣ Data Cleaning & Preparation

**Sheets cleaned:** `customer_demographic`, `customer_address`, `transactions`, `new_customer_list`.

Key steps:

- Removed **duplicate** customers and addresses.
- Standardized inconsistent formats:
  - Gender labels (`M/F`, `Male/Female`)  
  - State names (e.g., `NSW`, `New South Wales`)  
  - Job titles and job industries.
- Verified and corrected:
  - Date formats for `transaction_date` and `product_first_sold_date`.
  - Missing or invalid entries in critical fields.
- Ensured all tables could be **joined by `customer_id`** without data-type issues.

**Impact:**  
Created a **clean, consistent, analysis-ready dataset** from **4 tables and ~28K records**, improving reliability of all downstream analysis.

---

### 2️⃣ Customer Segmentation

Used `customer_demographic` + `customer_address` to understand **who the customers are**.

Segmentation dimensions:

- **Wealth Segment**
  - Counted customers by `wealth_segment` (e.g., *Mass Customer, High Net Worth, Affluent*).
  - Calculated **average tenure** per segment.

- **Gender**
  - Number of customers by gender.
  - Average `past_3_years_bike_related_purchases` by gender.

- **Job Industry Category**
  - Customers per `job_industry_category`.
  - Mix of `wealth_segment` inside each industry.

**Insights (examples):**

- Certain **wealth segments** have longer **average tenure**, indicating **loyal, high-value customers**.
- Specific job industries (e.g., *Financial Services, Manufacturing*) show a higher concentration of **High Net Worth** customers, making them priority targets for premium offerings.

---

### 3️⃣ Transaction & Revenue Analysis

Using the **19,445-row `transactions` table**:

- Built **monthly sales trends** using pivot tables:
  - Revenue by month
  - Volume of transactions by month  
  → helps identify **seasonality** and **peak months**.

- Analyzed **brand and product performance**:
  - Total revenue and average list price per **brand** and **product_line**.
  - Identified which combinations bring **most revenue** and **higher margins**.

- Identified **Top Customers**:
  - Total revenue per `customer_id`.
  - Ranked **Top N** customers by total spend.

**Insights (examples):**

- Sales show **clear peak periods**, ideal for aligning **marketing campaigns** and **inventory planning**.
- A small set of **brands and product lines** contribute a large share of revenue, supporting **focused product strategy**.
- A minority of customers generate **disproportionately high revenue**, confirming a **Pareto pattern (top customers = high impact)** and justifying **VIP/loyalty programs**.

---

### 4️⃣ New Customer Analysis

Using `new_customer_list` (1,000 rows):

- Segmented new customers by:
  - `wealth_segment`
  - `job_industry_category`
  - `state` / region

- Compared their profile to existing **high-value segments**.

**Insights:**

- Some new-customer segments strongly **resemble current profitable customers** in terms of wealth, industry, and geography.
- States/regions with higher **property valuation** and wealthy segments are strong candidates for **focused acquisition marketing**.

---

### 5️⃣ Customer Lifetime Value (CLV) Modeling

Built a **simplified CLV model** based on:

- **Average Purchase Value (APV)**  
  `APV = Total Revenue per Customer / Number of Transactions per Customer`

- **Purchase Frequency (PF)**  
  `PF = Total Transactions / Number of Unique Customers`

- **Customer Lifespan** (based on `tenure` from demographic data)

From these, CLV was approximated as:

> **CLV = (Average Purchase Value × Purchase Frequency) × Customer Lifespan**

CLV was then:

- Calculated at the **customer level**.
- Aggregated by:
  - Wealth Segment  
  - Job Industry  
  - State / region

**Key outcomes:**

- **High Net Worth** and certain industries have **significantly higher average CLV**.
- These segments should be prioritized in:
  - **Retention strategies** (VIP programs, personalized offers)  
  - **Cross-sell / upsell campaigns**  
  - **Geographical expansion decision-making**

---

## 📈 Metrics & Impact

This analysis is structured like a real consulting engagement and emphasizes measurable outcomes:

- **Data volume handled:**
  - `customer_demographic`: **4,000 rows × 13 columns**  
  - `customer_address`: **3,999 rows × 6 columns**  
  - `transactions`: **19,445 rows × 13 columns**  
  - `new_customer_list`: **1,000 rows × 23 columns**  
  → **~28K+ rows** across customer and transaction data.

- **Data quality improvement:**
  - Removed duplicates and standardized inconsistent categories across **thousands of rows** (gender, state, job industry, dates).
  - Produced a **clean, joined dataset** suitable for reliable reporting and modeling.

- **Customer & revenue insights:**
  - Monthly sales trends and brand analysis highlight **peak months** and **top-performing brands** for targeted promotions.
  - Segmentation and CLV help focus marketing on **higher-value segments** instead of treating all customers equally.

- **Business value:**
  - The project framework can be used to **optimize marketing spend**, **prioritize high-CLV customers**, and **target new customers** similar to the most profitable existing ones.

---

## 🚀 How to Open & Explore

1. Clone or download this repository.
2. Open `KPMG final project.xlsx` in **Microsoft Excel**.
3. Explore:
   - Raw data sheets: `customer_demographic`, `customer_address`, `transactions`, `new_customer_list`
   - Task sheets (e.g., `task2`, `task3`, `task4`, `task5`) for intermediate calculations and summaries.
   - Any dashboard/summary sheets that present **KPIs, charts, and tables**.

---

This project demonstrates:

- **Data cleaning & transformation** on **4+ tables and ~28K rows**.  
- **Customer segmentation, transaction analysis, and CLV modeling** using Excel.  
- Ability to create **pivot-based dashboards and executive summaries** with clear, actionable recommendations.

Example resume bullet you can reuse:

> **Analyzed** KPMG’s customer and transaction data in Excel (≈28K rows across four tables), **cleaning and joining** demographics, address, and 19K+ transactions to build customer segments, sales trends, and CLV metrics that highlight high-value customer groups and support targeted marketing and retention strategies.

