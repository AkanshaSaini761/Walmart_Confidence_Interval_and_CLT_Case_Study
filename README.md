# 🛒 Walmart Black Friday Purchase Analysis

## 🏢 About Walmart
**Walmart** is a globally recognized retail corporation, operating a vast chain of supercenters, discount stores, and grocery outlets. With **over 100 million** customers, Walmart is constantly looking for ways to better understand and serve its customer base.

## 🎯 Objective

The goal of this case study is to analyze customer purchase behavior during **Black Friday** and understand:
- Do **men** and **women** spend differently?
- How does **marital status**, **occupation**, and **age** affect purchase amount?
- How confident can we be in sample statistics when applied to the full population of **100 million+** customers?

## 📁 Dataset Overview

**📥 Dataset:** [walmart_data.csv](https://github.com/AkanshaSaini761/Walmart_Confidence_Interval_and_CLT_Case_Study/blob/main/walmart_data.csv) 

The dataset contains transactional data of over **550,000** purchases made during Black Friday sales.

| Column                    | Description                                       |
|---------------------------|---------------------------------------------------|
| `User_ID`                 | Unique identifier for each customer               |
| `Product_ID`              | Unique product code                               |
| `Gender`                  | Gender of the customer (`M` or `F`)               |
| `Age`                     | Age group in bins                                 |
| `Occupation`              | Encoded occupation of the customer                |
| `City_Category`           | Category of the city (A, B, C)                    |
| `Stay_In_Current_City_Years` | No. of years living in current city         |
| `Marital_Status`          | 0 = Unmarried, 1 = Married                        |
| `Product_Category`        | Encoded product category                          |
| `Purchase`                | Amount spent in transaction                       |

## 🔍 Exploratory Goals 

- Understand how gender affects spending patterns.
- Compare purchase behavior across different age groups, marital statuses, and occupations.
- Apply **Central Limit Theorem** to construct **confidence intervals** for average purchase.
- Examine **outliers**, **distribution**, and **demographic effects** on sales behavior.
- Generate business-friendly insights backed by statistical rigor.

## 🧪 Exploratory Data Analysis Highlights

### 📊 General Overview
- **Total Records:** 550,068
- **Unique Users:** 5,891
- **No missing or duplicate values** found.
- Data heavily skewed toward **male customers** (~75%).

### 🔢 Univariate & Bivariate Analysis
- Most purchases fall between **₹5,000 – ₹12,000**.
- Highest sales from **Product Categories 5, 1, and 8**.
- Prime spending age group: **26–35 years**
- City B shows **highest purchase volume**.
- Occupation codes **0, 4, and 7** are the top spenders.

### 📉 Outlier Detection & Treatment
- 2,677 outliers clipped using **IQR method**.
- Purchase distribution post-treatment is more centered and interpretable.


## 👨‍👩‍👧 Gender-Based Analysis

### ✅ Key Findings:
- **Males** spend significantly more than **females** (₹9428 vs ₹8726 average).
- Male spending shows **wider range and higher peak**.
- **Confidence Intervals** for spending do **not overlap** → Statistically significant difference.

### 🧪 Bootstrapped Confidence Intervals:
Sample Size = 100,000  
- **Males:** [9388, 9469]  
- **Females:** [8688, 8764]  
(At 99% confidence)


## 💍 Marital Status-Based Analysis

- Average spend for **unmarried**: ₹9257  
- Average spend for **married**: ₹9251  
- Very **small difference**; not statistically significant.

## 📊 Multivariate Highlights

- Gender impact persists across **cities, age brackets**, and **product categories**.
- **Females** prefer Product Categories 5 & 8.
- **Males** dominate in occupations 0, 4, and 7.
- Strongest age bracket: **26–35**, across all groups.


## 🧠 Insights & Interpretation

1. **Male customers spend more**, and confidence intervals confirm statistical significance.
2. **Unmarried customers** spend slightly more, though not statistically significant.
3. **Category 5** products dominate across all demographics.
4. Spending patterns are **similar across most city categories**.
5. **No strong correlation** between occupation and purchase amount (confirmed via heatmap).


## 💡 Business Recommendations

1. 🎯 **Target male customers** with premium offers during Black Friday.
2. 🛍️ **Promote Product Category 5** aggressively—it’s popular across all segments.
3. 💬 **Offer special bundles or discounts for female customers** to increase overall ticket size.
4. 📊 Leverage **age group 26–35** with exclusive deals and digital campaigns.
5. 🎁 Use confidence intervals to **predict campaign effectiveness** across demographics.

## 🛠️ Tools Used

- Python (`pandas`, `matplotlib`, `seaborn`, `scipy`, `numpy`)
- Central Limit Theorem, KDE plots, Histograms, Boxplots
- Confidence Interval bootstrapping
- Jupyter Notebook

## 📄 Output Report

All visualizations, detailed insights, and code are documented in this PDF:  
📎 [walmart_case_study_akansha_saini.pdf](https://github.com/AkanshaSaini761/Walmart_Confidence_Interval_and_CLT_Case_Study/blob/main/walmart_case_study_akansha_saini.pdf)
