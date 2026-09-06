# 🛒 Olist E-Commerce Analytics: Driving Customer Satisfaction in Brazil 🇧🇷

## 📌 Project Overview
Olist is a Brazilian e-commerce platform that connects small and medium merchants to major online marketplaces. Between 2016 and 2018, the platform experienced hyper-growth, scaling to over 1 million Reais in monthly revenue. However, as order volume surged, customer satisfaction began to decline. 

This project analyzes over **100,000 real operational orders** to uncover the root causes of customer dissatisfaction across delivery logistics, seller geography, product categories, and payment behavior[cite: 1]. 

## 🎯 Business Objective
To provide Olist leadership with a data-driven understanding of marketplace performance and deliver actionable recommendations to safely scale the platform without sacrificing customer loyalty[cite: 1].

## 📊 The Dataset
The analysis uses the [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce), originally published on Kaggle. It consists of 9 relational datasets containing:
* **Orders & Items:** 99K+ orders and 112K+ line items.
* **Customers & Sellers:** Geographic mapping via zip codes and coordinates.
* **Payments:** Installment behavior and payment types.
* **Reviews:** Post-purchase customer satisfaction scores (1 to 5 stars).
* **Products:** Dimensional data (weight, height, length) and categories.

## 🛠️ Tech Stack
* **Language:** Python
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Environment:** Google Colab / Jupyter Notebook

## 🚀 Key Insights & Findings

### 1. Delivery Delays Destroy Satisfaction
Missing the estimated delivery date is the primary driver of negative reviews. 
* Orders arriving **on time/early** average **4.29 stars**[cite: 1].
* Orders delayed by **1-7 days** drop to **3.18 stars**[cite: 1].
* Orders delayed by **14+ days** plummet to **1.71 stars**[cite: 1].

### 2. The Cross-State Shipping Bottleneck
Because the majority of sellers are concentrated in São Paulo (Southeast), orders shipped to the North and Northeast (e.g., Alagoas, Maranhão) require complex cross-state logistics[cite: 1]. These routes fail at a significantly higher rate, with states like Alagoas experiencing a **24.1% late delivery rate**[cite: 1].

### 3. Heavy Freight is Structurally Flawed
Product categories with high average weights suffer the worst review scores[cite: 1]. **Office Furniture** is the lowest-performing significant category (3.49 stars), weighed down by an average product weight of over 11 kg and R$40+ in freight costs[cite: 1].

### 4. Installments Unlock High-Value Carts
Credit cards dominate the platform. Customers paying in full have an Average Order Value (AOV) of R$101, while customers utilizing 7 to 10 installments have an AOV of **R$335**[cite: 1]. However, these high-value carts carry higher customer expectations[cite: 1].

## 💡 Actionable Recommendations
1. **De-risk Cross-State Logistics:** Launch targeted seller acquisition campaigns in the North and Northeast regions to build local inventory hubs and reduce reliance on long-haul transit[cite: 1].
2. **Recalibrate Delivery Algorithms:** Extend the algorithmic estimated delivery window for heavy categories (e.g., Furniture) to set more realistic expectations and avoid triggering the "late delay" threshold[cite: 1].
3. **Protect High-Installment Customers:** Implement proactive tracking notifications and priority customer service routing for orders utilizing 4+ credit card installments[cite: 1].

## 📁 Repository Structure
```text
├── datasets/                   # Contains the 9 Olist CSV files (Link to Kaggle above)
├── Olist_Analysis.ipynb        # Main Google Colab / Jupyter Notebook containing all code
├── Olist_Analysis_Report.pdf   # Executive summary and business report
└── README.md                   # Project documentation
