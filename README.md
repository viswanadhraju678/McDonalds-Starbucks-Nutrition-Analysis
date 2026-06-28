# 🍔☕ McDonald's vs Starbucks Nutrition Analysis using PySpark

![PySpark](https://img.shields.io/badge/PySpark-Data%20Processing-orange)
![Python](https://img.shields.io/badge/Python-Programming-blue)
![EDA](https://img.shields.io/badge/EDA-Analytics-green)
![Data Cleaning](https://img.shields.io/badge/Data-Cleaning-yellow)
![Data Engineering](https://img.shields.io/badge/Data-Engineering-red)
![GitHub](https://img.shields.io/badge/GitHub-Portfolio-black)

## 📊 PySpark Data Analysis | Data Cleaning | Data Engineering | Nutritional Analytics

🚀 End-to-End Nutritional Data Analysis Project built using PySpark to compare the nutritional characteristics of menu items from McDonald's and Starbucks.

---

# 📌 Project Overview

Consumers often judge the healthiness of a food item solely based on calories. However, nutritional health depends on several factors including:

* Calories
* Fat
* Carbohydrates
* Fiber
* Sugars
* Protein
* Sodium

This project analyzes and compares menu items from McDonald's and Starbucks to identify nutritional differences between their food and beverage products.

The project demonstrates real-world data engineering skills, including:

* Dataset Profiling
* Data Cleaning
* Schema Standardization
* Dataset Integration
* Exploratory Data Analysis
* Data Aggregation
* Business Insight Generation

---

# 🎯 Business Problem

Fast-food and coffee chains provide large amounts of nutritional information, but comparing products across brands is difficult because datasets often contain:

* Different schemas
* Missing values
* Duplicate records
* Different naming conventions
* Inconsistent nutritional attributes

The objective of this project was to build a unified analytical dataset and perform a comparative nutritional analysis using PySpark.

---

# 🛠 Technologies Used

| Technology       | Purpose                     |
| ---------------- | --------------------------- |
| Python           | Programming Language        |
| PySpark          | Large-scale Data Processing |
| Jupyter Notebook | Development Environment     |
| Pandas           | CSV Handling                |
| Git              | Version Control             |
| GitHub           | Project Portfolio           |

---

# 📂 Datasets Used

The project utilized four datasets.

## McDonald's Dataset

* mcd.csv

Contains nutritional information for:

* Burgers
* Breakfast meals
* Sandwiches
* Desserts
* Snacks
* Beverages

---

## Starbucks Datasets

* sb_food.csv
* sb_drinks.csv
* sb_drink_expanded.csv

These datasets contain:

* Food nutritional information
* Beverage nutritional information
* Expanded nutritional information including caffeine and vitamin data

---

# 🏗 Project Workflow

## Step 1: Dataset Profiling

Performed:

* Row and column analysis
* Schema inspection
* Duplicate detection
* Missing value analysis
* Data type validation

### Key Findings

| Dataset               | Duplicate Records |
| --------------------- | ----------------- |
| mcd.csv               | 0                 |
| sb_food.csv           | 0                 |
| sb_drink_expanded.csv | 0                 |
| sb_drinks.csv         | 22                |

Additional findings:

* One missing caffeine value detected.
* Placeholder values (`-`) identified.
* Mixed categorical values (`Varies`, `varies`) identified.

---

## Step 2: Data Cleaning & Standardization

Performed:

* Renamed `Unnamed:0` to `Item_Name`
* Replaced `-` values with NULL
* Converted nutritional columns into numeric data types
* Removed duplicate records
* Preserved caffeine values recorded as `Varies`

---

## Step 3: Common Schema Creation

A unified schema was created containing:

* Brand
* Source_File
* Category
* Item_Name
* Calories
* Fat
* Carbohydrates
* Fiber
* Sugars
* Protein
* Sodium
* Caffeine

All datasets were integrated into:

```python
master_nutrition_df
```

---

## Step 4: Exploratory Data Analysis (EDA)

Final dataset composition:

| Brand     | Total Records |
| --------- | ------------- |
| McDonalds | 260           |
| Starbucks | 510           |
| Total     | 770           |

EDA included:

* Dataset composition analysis
* Missing value analysis
* Nutritional aggregation
* Schema validation
* Product category analysis

---

# 📈 Product Type Distribution

| Brand     | Product Type | Count |
| --------- | ------------ | ----- |
| McDonalds | Drink        | 150   |
| McDonalds | Food         | 110   |
| Starbucks | Drink        | 397   |
| Starbucks | Food         | 113   |

---

# 🥤 Drinks Comparison

| Brand     | Avg Calories | Avg Fat | Avg Carbohydrates | Avg Sugars | Avg Sodium |
| --------- | ------------ | ------- | ----------------- | ---------- | ---------- |
| McDonalds | 299.47       | 7.73    | 50.27             | 44.64      | 128.43     |
| Starbucks | 180.38       | 2.85    | 104.05            | 32.96      | 20.00      |

### Key Findings

✅ Starbucks beverages contain:

* Lower calories
* Lower fat
* Lower sugar levels
* Significantly lower sodium

✅ McDonald's beverages contain:

* Slightly higher protein levels

---

# 🍔 Food Comparison

| Brand     | Avg Calories | Avg Fat | Avg Carbohydrates | Avg Protein | Avg Sodium |
| --------- | ------------ | ------- | ----------------- | ----------- | ---------- |
| McDonalds | 462.09       | 22.94   | 43.36             | 20.78       | 996.64     |
| Starbucks | 356.64       | 16.35   | 41.49             | 11.47       | N/A        |

### Key Findings

✅ Starbucks food products contain:

* Lower calories
* Lower fat

✅ McDonald's food products contain:

* Higher protein levels

---

# 📊 Overall Brand Comparison

| Brand     | Avg Calories | Avg Fat | Avg Sugars | Avg Protein |
| --------- | ------------ | ------- | ---------- | ----------- |
| McDonalds | 368.27       | 14.17   | 29.42      | 13.34       |
| Starbucks | 226.70       | 6.40    | 32.96      | 7.77        |

---

# ⚠ Challenges Faced

### Challenge 1: Different Dataset Schemas

The four datasets contained different column names and structures.

**Solution:** Created a common schema and standardized all columns.

---

### Challenge 2: Duplicate Records

The Starbucks drinks dataset contained 22 duplicate records.

**Solution:** Performed duplicate detection and removed duplicates before analysis.

---

### Challenge 3: Missing Values

Several nutritional attributes were unavailable in some datasets.

**Solution:** Preserved missing values as NULL instead of replacing them with artificial values.

---

### Challenge 4: Mixed Caffeine Values

The caffeine column contained:

* Numeric values
* `Varies`
* `varies`
* NULL values

**Solution:** Preserved categorical values rather than incorrectly converting them.

---

# 💡 Business Insights

* Starbucks beverages generally contain fewer calories and significantly lower sodium levels.
* McDonald's food products provide higher protein content.
* No single nutritional metric determines whether a product is healthy.
* Nutritional evaluation should consider multiple attributes simultaneously.

---

# 📁 Repository Structure

```text
McDonalds-Starbucks-Nutrition-Analysis
│
├── data/
├── notebooks/
│   └── Nutritional_Snack_analysis.ipynb
│
├── reports/
│   ├── Analysis_Report.pdf
│   └── Challenges_and_Solutions.pdf
│
├── screenshots/
│
└── README.md
```

---

# 🚀 Skills Demonstrated

* PySpark DataFrames
* Data Profiling
* Data Cleaning
* Data Transformation
* Data Standardization
* Exploratory Data Analysis
* Data Aggregation
* Problem Solving
* Documentation
* Git & GitHub

---

# 👨‍💻 Author

**Viswanadh Raju**

Aspiring Data Engineer passionate about:

* Data Engineering
* PySpark
* Azure
* SQL
* ETL Pipelines
* Data Analytics
* Cloud Technologies

---

⭐ If you found this project useful, feel free to explore the repository and connect.
