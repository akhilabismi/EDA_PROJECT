# 🏠 Airbnb Listings Data Analysis Project

## 📋 Project Overview

This project performs an **end-to-end Exploratory Data Analysis (EDA)** on an Airbnb listings dataset to understand pricing patterns, demand, and factors affecting listing performance.

The analysis focuses on answering key business questions such as:

* Which locations are most expensive?
* Which room types generate higher revenue?
* Do reviews influence price and demand?
* How does price change over time?

The project follows a structured **4-notebook industry workflow**:
Data Understanding → Cleaning → Exploration → Statistical Analysis → Insights.

---

## 📅 Progress Log

### **Day 1: Data Understanding & Profiling**

* Loaded dataset and inspected structure (`shape`, `info`, `describe`).
* Identified numerical, categorical, and date columns.
* Detected missing values in:

  * `last_review`
  * `reviews_per_month`
* Observed extreme values in the `price` column.
* Logged initial data quality issues.

---

### **Day 2: Data Cleaning & Preprocessing**

* Converted `last_review` to datetime.
* Handled missing values:

  * `reviews_per_month` → filled with 0
  * text columns → filled with “unknown”
* Removed extreme price outliers using **IQR method**.
* Created `log_price` to reduce skewness.
* Standardized categorical values.

Dataset became clean and ready for analysis.

---

### **Day 3: Visual Exploration (EDA)**

#### **Univariate Analysis**

* Price distribution is heavily right-skewed.
* Majority of listings are low to mid-priced.
* Entire homes and private rooms dominate the market.

#### **Bivariate Analysis**

* Entire homes have highest prices.
* Private rooms receive more reviews (higher demand).
* Some locations have significantly higher prices.
* Weak correlation between price and numeric features.

---

### **Day 4: Statistical Testing & Feature Engineering**

#### Feature Engineering

Created new variables:

* `host_type`
* `price_per_review`
* time-based features from review dates

#### Statistical Tests

* **T-Test:** Entire homes cost significantly more than private rooms (p < 0.05).
* **ANOVA:** Price differs significantly across locations (p < 0.05).
* **Chi-Square:** Room type distribution varies by location.

These tests statistically validated EDA findings.

---

## 📈 Key Business Insights

* **Location drives pricing:** Certain neighbourhoods are significantly more expensive.
* **Entire homes generate highest revenue** but receive fewer bookings.
* **Affordable listings receive more reviews**, indicating higher demand.
* **High prices reduce booking frequency.**
* **Private rooms dominate booking volume.**
* Price distribution shows most listings fall within an affordable range.

---

## 🛠️ Tech Stack

* **Python:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Statistics:** Scipy
* **Environment:** Jupyter Notebook

---

## 📊 Project Structure

```
01_data_overview.ipynb
02_cleaning_preprocessing.ipynb
03_univariate_bivariate_eda.ipynb
04_stats_time_features_final_insights.ipynb
```

---

## 🎯 Conclusion

This project demonstrates a complete real-world data analysis workflow:

* Data understanding
* Cleaning & preprocessing
* Visual exploration
* Statistical validation
* Business insights

The findings help Airbnb hosts and analysts make informed decisions about:

* Pricing strategy
* Location targeting
* Room type selection
* Demand patterns

---

**Final Output:** Actionable insights for improving Airbnb listing performance and pricing strategy.
