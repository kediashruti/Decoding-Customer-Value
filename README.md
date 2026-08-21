# Decoding Customer Value — A Retention & Loyalty Analysis

A data analytics project focused on understanding customer value, loyalty, repeat purchasing behavior, and dependence on discounts for a fashion retail brand.

The main question of the project is:

> **Are we building loyal customers, or are we relying on discounts to make sales?**

The project uses customer behavioral data from around **3,900 customers** to identify valuable customer groups, understand purchasing patterns, study promotional dependency, and create a practical retention strategy. The project brief specifically requires loyalty to be created from the available data because the dataset does not contain a ready-made loyalty score or churn label. 

---

## 📌 Project Overview

The fashion brand sells clothing, accessories, footwear, and outerwear directly to customers across the United States.

Although the company has customer data, it does not have a structured way to understand:

* Which customers are genuinely loyal
* Which customers mainly purchase when discounts are available
* What behaviors are linked with higher customer value
* Which categories have more repeat purchases
* Which locations show strong customer demand
* What the ideal customer looks like
* How discounts can be reduced without losing valuable customers

This project uses **Python, SQL, and data visualization** to turn the raw customer data into useful business insights.

The project is designed around the five main business questions given in the project brief. 

---

# 🎯 Business Questions

The analysis focuses on the following questions:

1. **Who are the genuinely loyal customers and who mainly buys when there is a discount?**
2. **What customer behaviors are linked with higher customer value?**
3. **Which categories and purchase patterns are linked with repeat purchasing?**
4. **Which locations show strong organic demand instead of discount-driven demand?**
5. **What does the ideal customer look like?**

These questions form the main analytical framework of the project. 

---

# 📂 Dataset

The dataset contains approximately **3,900 customer records**.

Each row represents a customer and contains information about their demographics, purchases, preferences, discounts, subscription status, satisfaction, and purchasing frequency.

### Main columns

| Column                   | Description                             |
| ------------------------ | --------------------------------------- |
| `Customer ID`            | Unique customer identifier              |
| `Age`                    | Customer age                            |
| `Gender`                 | Customer gender                         |
| `Item Purchased`         | Product purchased                       |
| `Category`               | Product category                        |
| `Purchase Amount (USD)`  | Amount spent on the purchase            |
| `Location`               | Customer location                       |
| `Size`                   | Product size                            |
| `Color`                  | Product color                           |
| `Season`                 | Purchase season                         |
| `Review Rating`          | Customer review rating                  |
| `Subscription Status`    | Whether the customer has a subscription |
| `Shipping Type`          | Shipping method                         |
| `Discount Applied`       | Whether a discount was applied          |
| `Promo Code Used`        | Whether a promo code was used           |
| `Previous Purchases`     | Number of previous purchases            |
| `Payment Method`         | Customer payment method                 |
| `Frequency of Purchases` | How frequently the customer purchases   |

---

# 🛠️ Tools Used

### Python

* Pandas
* NumPy

Used for:

* Data cleaning
* Data quality checks
* Feature engineering
* Customer segmentation
* Exploratory analysis

### SQL

* SQLite
* SQL queries

Used for:

* Customer segmentation
* Customer value analysis
* Category analysis
* Geographic analysis
* Promotion dependency analysis

### Data Visualization

* Matplotlib
* Seaborn

Used to create charts that make the findings easier to understand.

### Dashboard

* Power BI
* Founder dashboard

The project brief requires a four-panel dashboard designed for a non-technical founding team. 

---

# 🔄 Project Workflow

```text
Raw Customer Data
        ↓
Data Cleaning
        ↓
Data Quality Checks
        ↓
Feature Engineering
        ↓
Customer Value Analysis
        ↓
Loyalty Definition
        ↓
SQL Customer Segmentation
        ↓
Promotion Dependency Analysis
        ↓
Category & Geography Analysis
        ↓
Dashboard
        ↓
Retention Strategy
        ↓
Business Recommendations
```

---

# 🧹 Data Cleaning

The raw dataset was checked and prepared before analysis.

The cleaning process included:

* Checking missing values
* Checking duplicate records
* Checking data types
* Standardizing column names
* Checking categorical values
* Checking numerical values
* Preparing the data for SQL analysis

The goal was to make the dataset consistent and suitable for further analysis.

---

# 🔧 Feature Engineering

The dataset does not directly provide all the metrics needed for the business questions.

Therefore, new features were created from the existing columns.

The project brief specifically states that every engineered feature should have a clear business purpose rather than being created just for the sake of analysis. 

Some of the important features include:

### Customer Value

A customer value measure was created using available purchase-related information.

This helps separate customers into different value groups.

### Value Tier

Customers were divided into groups such as:

* Low Value
* Medium Value
* High Value

This makes it easier to compare customer behavior across different value levels.

### Promotion Dependency

A promotion dependency measure was created using discount and promotional information.

It helps answer:

> Are customers purchasing because they value the brand, or because a promotion is available?

### Satisfaction Flag

Review ratings were used to create a simple satisfaction indicator.

### Purchase Frequency

The available purchase-frequency information was converted into a form that can be used to compare customers based on how regularly they purchase.

---

# ⭐ Defining Customer Loyalty

One of the most important parts of this project is defining **loyalty**.

The dataset does not contain a loyalty score, churn label, or timestamp. Therefore, loyalty cannot simply be assumed. The project requires at least **two different loyalty definitions**, testing them, and selecting the better one based on evidence from the data. 

Two different approaches were therefore tested using different combinations of customer behavior.

The definitions were compared based on factors such as:

* Purchase behavior
* Purchase frequency
* Customer value
* Satisfaction
* Relationship with revenue

The final loyalty definition was selected based on how well it separated valuable customers and represented actual customer behavior.

---

# 🗄️ SQL Analysis

After cleaning and feature engineering, the customer dataset was loaded into SQLite.

SQL was then used to answer the main business questions.

### Customer Value

The analysis compares high-value and low-value customers based on:

* Purchase amount
* Previous purchases
* Purchase frequency
* Satisfaction
* Promotion dependency

### Promotion Dependency

Customers were compared based on whether their purchasing behavior showed a strong relationship with promotions.

This helps identify customers who may continue purchasing without needing regular discounts.

### Category Analysis

Different product categories were compared using:

* Previous purchases
* Purchase amount
* Customer value
* Purchase frequency

This helps identify categories that may act as entry points and categories associated with stronger repeat purchasing.

### Geographic Analysis

Customer locations were compared based on:

* Customer count
* Average purchase amount
* Previous purchases
* Promotion dependency

The aim is not simply to find locations with the most customers, but locations where customers spend more while showing lower dependence on promotions.

This is described in the project brief as identifying regions with genuine brand demand. 

---

# 📊 Dashboard

A four-panel founder dashboard was created to present the main findings in a simple way.

### 1. Customer Value Pyramid

Shows how customers are distributed across different value levels.

### 2. Promotion Dependency vs Retention

Shows which customer segments depend more on discounts and which customers purchase with less promotional support.

### 3. Geographic Opportunity

Shows locations with stronger spending and lower promotion dependency.

### 4. Category Funnel

Shows categories associated with lower purchase history and categories associated with higher repeat purchasing.

These four views are based on the dashboard requirements given in the project statement. 

---

# 💡 Key Insights

The analysis is designed to identify patterns such as:

* Customers with stronger repeat-purchase behavior tend to represent higher customer value.
* Promotion-dependent customers need to be treated differently from customers who purchase without discounts.
* Some product categories may be more strongly associated with repeat purchasing.
* Some locations may have strong customer spending without high promotional dependency.
* Customer value is influenced by purchasing behavior rather than a single variable.

The exact numbers and findings are presented in the notebook and dashboard.

---

# 📈 Retention Strategy

The final stage of the project converts the analysis into business recommendations.

The goal is not simply to say:

> "Reduce discounts."

Instead, the project identifies **which customer segment should receive fewer discounts, why, when the change should happen, and what metric should be monitored.**

The project brief specifically requires the promotional sunset plan to include:

* Target customer segment
* Trigger behavior
* Rollout timeline
* Metric to monitor
* Expected benefit
* Possible trade-off 

### Example strategy

High-value customers who repeatedly purchase and show low promotional dependency can be gradually moved away from regular discounts.

Instead of removing discounts suddenly, the brand can test:

```text
Current discount
      ↓
Reduced discount
      ↓
Targeted offer
      ↓
Loyalty benefit
      ↓
Organic purchasing
```

The main metric to monitor would be whether purchase behavior remains stable after reducing promotional support.

---

# 👤 Ideal Customer Profile

The project also creates a data-backed profile of the brand's most valuable customer.

The profile considers factors such as:

* Age
* Gender
* Purchase frequency
* Previous purchases
* Average purchase amount
* Preferred category
* Payment method
* Satisfaction
* Promotion dependency

The purpose is to give the marketing team a clear idea of the type of customer they should focus on acquiring and retaining.

The project brief specifically asks for an ideal customer profile that is detailed enough to support actual marketing decisions. 

---




# 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone <your-repository-link>
```

### 2. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn
```

SQLite is available through Python's built-in `sqlite3` library.

### 3. Open Jupyter Notebook

```bash
jupyter notebook
```

### 4. Run

Open:

```text
Decoding_Customer_Value.ipynb
```

and run the cells from top to bottom.

---


# 🎯 Final Outcome

The project converts raw customer data into a simple retention strategy:

```text
Customer Data
      ↓
Understand Customer Behavior
      ↓
Measure Customer Value
      ↓
Define & Test Loyalty
      ↓
Identify Promotion Dependency
      ↓
Find Valuable Customer Segments
      ↓
Identify Strong Categories & Locations
      ↓
Build Ideal Customer Profile
      ↓
Create Retention Strategy
```

The final goal is to help the brand answer one important question:

> **Are we building genuine customer loyalty, or are we depending on promotions to keep customers buying?**

The analysis provides the data, SQL queries, visualizations, and recommendations needed to make that decision. The project brief describes the expected outcome as a customer-intelligence solution that gives the brand a clear and actionable answer to this question. 


