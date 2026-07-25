# devlab-internship-Week3-Task3
# 🛒 Olist E-Commerce Customer Retention & Delivery Performance Analysis

## 📌 Project Overview

This project analyzes customer purchasing behavior using the Brazilian Olist E-Commerce dataset. The main objective is to understand customer retention through Cohort Analysis and investigate how delivery time influences customer satisfaction.

The analysis combines customer, order, order item, and review datasets to identify purchasing patterns, evaluate customer loyalty, and generate business recommendations based on real data.

---

# 🎯 Objectives

The main objectives of this project are:

- Analyze customer retention using Cohort Analysis.
- Measure customer repurchase behavior over time.
- Calculate the average delivery time.
- Investigate the relationship between delivery time and customer review scores.
- Generate actionable business insights to improve customer satisfaction and retention.

---

# 📂 Dataset

https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

---

# 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

# 📊 Data Preparation

The following preprocessing steps were performed:

- Loaded all datasets
- Merged datasets using `order_id` and `customer_id`
- Filtered only delivered orders
- Converted purchase and delivery dates to datetime format
- Created `YearMonth`
- Identified each customer's first purchase month (`CohortMonth`)
- Calculated `CohortIndex`
- Built Cohort Pivot Table
- Calculated Retention Rate
- Created delivery time buckets
- Analyzed customer review scores based on delivery duration

---

# 📈 Visualizations

The project includes the following visualizations:

- Customer Retention Heatmap
- Cohort Size Bar Chart
- Average Review Score by Delivery Time Bucket

---

# 🔍 Key Findings

- The analysis includes only **delivered orders**, ensuring accurate evaluation of completed purchases.
- Customer retention decreases consistently after the first purchase.
- Most customers do not return after their initial order.
- Delivery time has a negative relationship with customer satisfaction.
- Faster deliveries receive noticeably higher review scores than delayed deliveries.
- Larger cohorts provide valuable insights into successful customer acquisition periods.

---

# 💡 Business Insights

## 1. Customer satisfaction is generally high

The average review score across all delivered orders is **4.09/5**, indicating that most customers are satisfied with their shopping experience. Although the overall satisfaction level is positive, there is still room for improvement in customer experience.

**Recommendation**

Continue monitoring customer feedback and identify the main reasons behind low ratings to improve overall service quality.

---

## 2. Delivery performance has a measurable impact on customer satisfaction

The average delivery time is **12.01 days**. Correlation analysis produced a coefficient of **-0.30**, indicating a **moderate negative relationship** between delivery time and customer review scores.

This means that customers generally give lower ratings when delivery takes longer.

**Recommendation**

Reducing delivery time should be considered a business priority. Improving logistics operations and collaborating with more efficient shipping partners can increase customer satisfaction.

---

## 3. Faster deliveries lead to better customer experience

The delivery bucket analysis shows that orders delivered within shorter time periods receive higher average review scores compared to delayed deliveries.

Although the overall customer satisfaction remains positive, long delivery times gradually reduce customer ratings.

**Recommendation**

Set delivery time targets and continuously monitor delayed shipments to maintain a high level of customer satisfaction.

---

## 4. Customer retention decreases after the first purchase

The cohort retention analysis demonstrates that customer retention steadily declines over time. Most customers make only one purchase and do not return in subsequent months.

This indicates that customer acquisition alone is not sufficient for sustainable business growth.

**Recommendation**

Introduce loyalty programs, personalized product recommendations, discount coupons, and email marketing campaigns to encourage repeat purchases.

---

## 5. Cohort Analysis provides valuable marketing insights

Comparing different customer cohorts makes it possible to identify periods with stronger customer retention and evaluate the effectiveness of acquisition campaigns.

Understanding which cohorts perform better helps businesses optimize future marketing strategies and allocate budgets more efficiently.

**Recommendation**

Analyze high-performing cohorts to identify successful marketing initiatives and replicate them in future campaigns.

---

## 6. Delivery time should be monitored as a key business KPI

Since delivery time directly influences customer satisfaction, it should be tracked as one of the company's operational Key Performance Indicators (KPIs).

Monitoring this metric regularly enables businesses to identify logistics issues before they significantly affect customer experience.

**Recommendation**

Track average delivery time, delayed deliveries, and customer ratings through interactive dashboards to support data-driven decision making.

# 📌 Final Conclusion

This analysis demonstrates that customer retention and delivery performance are closely connected to long-term business success.

Although the overall customer satisfaction is relatively high (**4.09/5**), the analysis reveals that longer delivery times negatively influence customer ratings (**correlation = -0.30**). Additionally, cohort analysis indicates that customer retention declines steadily after the first purchase, highlighting the importance of retention-focused marketing strategies.

By improving delivery efficiency, implementing customer loyalty programs, and continuously monitoring retention metrics, Olist can enhance customer experience, increase repeat purchases, and support sustainable business growth.
---

