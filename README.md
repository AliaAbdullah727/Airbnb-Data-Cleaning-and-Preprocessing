
# 🏡 Airbnb Listings — Data Cleaning & Quality Validation

### Turning messy data into reliable, analysis-ready information.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google_Colab-F9AB00?style=flat-square&logo=googlecolab&logoColor=white)

## 📌 Project Overview

This project focuses on cleaning and validating a large Airbnb Listings dataset covering **10 cities**, using Python and Pandas.

The goal was to prepare a reliable dataset for further analysis and Power BI dashboard development.

Rather than automatically removing missing values or outliers, each cleaning decision was based on the meaning of the variable and its potential impact on the analysis.

## 📊 Dataset Summary

| Metric | Value |
|---|---:|
| Original records | 279,712 |
| Cleaned records | 279,599 |
| Original columns | 33 |
| Cities covered | 10 |
| Zero-price records excluded | 113 |

## 🔍 Data Cleaning Process

### 1. Data Inspection

- Examined dataset dimensions, column types, and descriptive statistics.
- Investigated missing values across numerical and categorical features.
- Checked duplicate records and primary-key uniqueness.
- Identified unusual values and inconsistencies.

### 2. Missing-Value Treatment

Different approaches were used depending on the nature of each variable.

| Variable | Treatment |
|---|---|
| Categorical host attributes | Assigned `Unknown` where appropriate |
| Host response and acceptance rates | Preserved missing values |
| Review scores | Preserved missing values |
| Bedrooms | Group-based mode imputation |
| Host registration dates | Preserved missing dates |

For `bedrooms`, missing values were estimated using listings with similar:

- Room types
- Property types
- Accommodation capacities

The imputation results were validated to ensure that bedroom counts remained whole numbers.

### 3. Price & Outlier Analysis

Price distributions were examined separately across cities.

**Key observations:**
- Prices were strongly right-skewed.
- 113 zero-price records were identified and excluded after inspection.
- Extreme prices were investigated rather than automatically removed.
- Currency differences between cities were considered when planning price comparisons.

**Important:** Statistical outliers were not automatically treated as data errors.

### 4. Data Consistency & Validation

- Verified uniqueness of `listing_id`.
- Investigated inconsistencies in `host_total_listings_count`.
- Distinguished reported host listing counts from counts observed within the dataset.
- Rechecked data types, missing values, and duplicate records.
- Validated the exported dataset before importing it into Power BI.

## ✅ Final Results

The cleaning process produced an analysis-ready dataset containing **279,599 listings**.

The resulting dataset preserves meaningful information while addressing identified quality issues.

Some missing values were intentionally retained to avoid introducing unsupported assumptions.

## 🛠️ Technologies

- **Python** — Data processing
- **Pandas** — Data cleaning and validation
- **NumPy** — Numerical operations
- **Google Colab** — Development environment


## 💡 Key Takeaway

**Good data cleaning is not about eliminating every null or outlier.**

It is about understanding the data, making justified decisions, and validating the results.

A missing value does not always need imputation, and an extreme observation is not necessarily an error.

## 👩‍💻 About Me

I'm **Alia Abdullah Al-Qadri**, a Data Analyst working with Python, Pandas, SQL, Excel, and Power BI.

I specialize in data cleaning, validation, statistical analysis, and dashboard development.

### 📬 Let's Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/alia-al-qadri-a1b8b939b/)

[![GitHub](https://img.shields.io/badge/GitHub-Portfolio-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/AliaAbdullah727)

---

⭐ **Clean Data • Reliable Analysis • Better Decisions**
