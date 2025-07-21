# 📊 Restaurant Sales Analysis - Q1 2003

## 📖 Introduction

This project presents a **first-quarter data analysis for a restaurant business in 2003**, using **Microsoft Excel** to uncover patterns in customer orders, product performance, and sales trends. The dataset consists of two related tables:

- `Menu_item`
- `Order_details`

The objective is to transform raw transactional data into meaningful business insights through Excel-based techniques such as **PivotTables**, **dynamic dashboards**, and **visual storytelling**. This analysis highlights key areas including:

- **Customer order patterns and preferences**
- **Revenue distribution by product and time**
- **Menu performance by category and item**

---

## 📑 Table of Contents
 
1. [📌 Project Overview](#-project-overview)  
2. [🎯 Project Scope](#-project-scope)  
3. [💼 Business Objectives](#-business-objectives)  
4. [📄 Document Purpose](#-document-purpose)  
5. [🧩 Use Case](#-use-case)  
6. [🗂️ Data Source](#️-data-source)  
7. [🧾 Dataset Overview](#-dataset-overview)  
8. [🧹 Data Cleaning and Processing](#-data-cleaning-and-processing)  
9. [📊 Data Analysis and Insights](#-data-analysis-and-insights)  
10. [✅ Recommendations](#-recommendations)  
11. [📌 Conclusion](#-conclusion)  
12. [📁 Repository Contents](#-repository-contents)  

---

## 📌 Project Overview

This project focuses on conducting a **comprehensive analysis of restaurant sales data** using **Microsoft Excel**. The dataset, sourced from **Maven Analytics**, includes detailed transactional records covering:

- `order_details_id`
- `order_id`
- `order_date`
- `order_time`
- `item_id`
- `menu_item`
- `item_name`
- `category`
- `price`

These records span multiple product categories and reflect the **ordering behavior of customers during the first quarter of 2003** for a restaurant business.

The project simulates a **real-world business intelligence scenario** by combining raw order details and menu metadata to uncover valuable operational insights. Through the use of **PivotTables**, **data cleaning techniques**, and an **interactive Excel dashboard**, the analysis reveals trends in **customer behavior**, **product performance**, and **revenue generation**.

The goal of this analysis is to **derive actionable business insights** and **inform strategic decisions** for **menu optimization and revenue growth**, equipping stakeholders with the data-driven clarity required to improve operational efficiency and profitability.

---

## 🎯 Project Scope

The scope of this project is limited to the analysis of **Q1 2003** restaurant sales data. The aims are to:

- Track sales volume and revenue by item and category  
- Uncover product popularity and customer preferences  
- Identify peak times for sales activity  
- Provide visual and interactive summaries using Excel  

---

## 💼 Business Objectives

The business objectives of this analysis are to:

- Support **menu optimization** and **revenue growth strategies**  
- Identify **high-performing** and **underperforming** products  
- Assist in **time-based resource planning** and **staffing**  
- Enable **data-driven marketing campaigns** through sales insights

---

## 📄 Document Purpose

This documentation serves to:

- Describe the analytical process from raw data to insight  
- Outline methodology and tools used in analysis  
- Present actionable findings through dashboard visuals  
- Offer recommendations for operational improvements

---

## 🧩 Use Case

This analysis benefits multiple stakeholders:

### 🔹 Business Owners & Management
- **Decision-Making Support:** Sales trends and product performance analysis enable better strategic decisions
- **Revenue Optimization:** Identify high-demand products and peak sales periods for pricing and promotion strategies

### 🔹 Marketing Team  
- **Targeted Campaigns:** Segment customers and products for focused marketing efforts
- **Promotional Strategies:** Maximize impact by targeting high-traffic periods with effective promotions 

### 🔹 Operations Team  
- **Staffing Efficiency:** Optimize staff scheduling based on sales patterns
- **Process Improvement:** Enhance service quality and kitchen operations by understanding order volumes

This comprehensive analysis provides the insights needed to enhance customer satisfaction, improve efficiency, and drive business growth.

---

## 🗂️ Data Source

- **Provider:** [Maven Analytics](https://app.mavenanalytics.io/datasets?order=-fields.dateAdded&search=restaurant+orders)  
- **Type:** Real-world, simulated business dataset  
- **Format:** Excel tables (`Menu_item` and `Order_details`)

---

## 🧾 Dataset Overview

### Tables Included:

- `Menu_item`: item_id, item_name, category and price  comprising of 128 records (32 rows and 4 columns)
- `Order_details`: order_id, order_date, order_time, item_id comprising of 61,170 records (12,234 rows and 5 columns) 

### Period Covered:  
- January 1 to March 31, 2003 (Q1)

---

  ## 🧹 Data Cleaning and Processing

- **Merged tables using `item_id`:**  
  The `Menu_item` and `Order_details` tables were merged to create a consolidated dataset for comprehensive analysis.  
  The `item_name`, `category`, and `price` columns were extracted from the `Menu_item` table and combined with the `Order_details` table using **INDEX-MATCH functions** in Excel.

  **Formulas used:**
  - `item_name`:  
    ```excel
    =INDEX(Menu_Items[item_name], MATCH([@[item_id]], Menu_Items[menu_item_id], 0))
    ```
  - `category`:  
    ```excel
    =INDEX(Menu_Items[category], MATCH([@[item_id]], Menu_Items[menu_item_id], 0))
    ```
  - `price`:  
    ```excel
    =INDEX(Menu_Items[price], MATCH([@[item_id]], Menu_Items[menu_item_id], 0))
    ```

- **Removed duplicates and handled missing values:**  
  Checked for and removed duplicate entries to ensure data quality and accuracy.

- **Extracted new columns (`Day` and `Month`) from `order_date`:**  
  Derived columns were created using **TEXT functions** in Excel to enhance time-based analysis.

  **Formulas used:**
  - `Day`:  
    ```excel
    =TEXT([@[order_date]], "DDDD")
    ```
  - `Month`:  
    ```excel
    =TEXT([@[order_date]], "MMMM")
    ```

- **Verified and standardized price and time formats:**  
  Ensured the `price` and `order_time` columns were correctly formatted and consistent throughout the dataset.

---

## 📊 Data Analysis and Insights

Key insights revealed include:

- 🍽️ **Top-selling menu items** by revenue and volume


- ⏰ **Sales peaks** during weekend lunch and dinner hours  
- 🥗 **Category performance**   
- ⚠️ **Low-performing items** identified for review  

---

## ✅ Recommendations

- Focus marketing on best-sellers through promotions or bundles  
- Phase out or rework low-selling products  
- Align staff shifts with demand trends to reduce overhead  
- Introduce loyalty incentives during low-sale hours  

---

## 📌 Conclusion

This Excel-based analysis demonstrates how raw restaurant data can be transformed into powerful business intelligence. By evaluating sales patterns, menu trends, and revenue flow, the business can make informed decisions that enhance service delivery, customer satisfaction, and profitability.

---

## 📸 Dashboard Preview



> *Sample Excel dashboard showing top selling items, low performing items,category performance, sales peak, and high spending order with its menu items.*

---

## 📁 Repository Contents

- `RAW DATASET.xlsx` – Original data tables  
- `ANALYZED DATASET AND DASHBOARD.xlsx` – Cleaned data + final dashboard  
- `README.md` – Project documentation  
