# McDonald's vs Starbucks Nutrition Analysis using PySpark

## Project Overview

This project analyzes and compares the nutritional characteristics of menu items from McDonald's and Starbucks using PySpark.

The objective was to evaluate nutritional differences between the two brands by analyzing calories, fat, carbohydrates, fiber, sugars, protein, sodium, and caffeine. The project demonstrates practical data engineering and analytical skills including data profiling, data cleaning, schema standardization, dataset integration, exploratory data analysis (EDA), and nutritional comparison reporting.

---

## Business Problem

Consumers often assume one fast-food brand is healthier than another. However, nutritional quality depends on multiple factors such as calories, fat, sugar, sodium, carbohydrates, fiber, and protein.

This project investigates:

* Which brand offers lower-calorie products?
* Which brand contains less sugar and sodium?
* Which brand provides higher protein content?
* How do food products compare separately from beverage products?
* Can data engineering techniques be used to build a reliable nutritional comparison framework?

---

## Technologies Used

* Python
* PySpark
* Pandas
* Jupyter Notebook
* Git
* GitHub

---

## Dataset Overview

Four nutritional datasets were used in this analysis.

| Dataset               | Records | Description                                                        |
| --------------------- | ------- | ------------------------------------------------------------------ |
| mcd.csv               | 260     | McDonald's food and beverage nutritional information               |
| sb_drinks.csv         | 177     | Starbucks drinks dataset                                           |
| sb_drink_expanded.csv | 242     | Detailed Starbucks beverage dataset including caffeine information |
| sb_food.csv           | 113     | Starbucks food products dataset                                    |

### Data Quality Issues Identified

During the profiling stage, several data quality issues were identified:

* 22 duplicate records in sb_drinks.csv
* Missing caffeine values
* Placeholder values represented as "-"
* Mixed categorical values such as "Varies" and "varies"
* Different schemas and attribute names across datasets

---

## Data Engineering Workflow

### Step 1 – Dataset Profiling

Performed comprehensive profiling on all datasets, including:

* Row and column count analysis
* Schema inspection
* Data type validation
* Duplicate record detection
* Missing value identification
* Dataset structure analysis

### Step 2 – Data Cleaning and Standardization

Implemented multiple data quality improvements:

* Removed 22 duplicate records from Starbucks drinks dataset
* Replaced placeholder "-" values with NULL
* Renamed inconsistent column names
* Converted nutritional attributes into numeric data types
* Preserved valid categorical caffeine values ("Varies")
* Standardized attribute formats across datasets

### Step 3 – Common Schema Creation

Designed a unified schema to enable comparison across all datasets.

Common schema fields:

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

### Step 4 – Dataset Integration

All cleaned datasets were merged into a master analytical dataset.

Final dataset composition:

| Brand      | Records |
| ---------- | ------- |
| McDonald's | 260     |
| Starbucks  | 510     |
| Total      | 770     |

### Step 5 – Exploratory Data Analysis

Performed:

* Brand-level nutritional analysis
* Source-file analysis
* Missing value assessment
* Nutritional aggregations
* Food vs beverage comparison
* Product category analysis
* Overall health-oriented nutritional evaluation

---

## Key Results

### Product Distribution

| Brand      | Food Items | Drink Items |
| ---------- | ---------- | ----------- |
| McDonald's | 110        | 150         |
| Starbucks  | 113        | 397         |

---

### Beverage Comparison

| Metric            | McDonald's | Starbucks |
| ----------------- | ---------- | --------- |
| Avg Calories      | 299.47     | 180.38    |
| Avg Fat           | 7.73       | 2.85      |
| Avg Carbohydrates | 50.27      | 104.05    |
| Avg Sugars        | 44.64      | 32.96     |
| Avg Sodium        | 128.43     | 20.00     |

#### Key Findings

* Starbucks beverages contained significantly fewer calories.
* Starbucks beverages contained lower fat levels.
* Starbucks beverages contained lower sugar content.
* Starbucks beverages contained substantially lower sodium levels.
* McDonald's beverages contained slightly higher protein levels.

---

### Food Comparison

| Metric            | McDonald's | Starbucks |
| ----------------- | ---------- | --------- |
| Avg Calories      | 462.09     | 356.64    |
| Avg Fat           | 22.94      | 16.35     |
| Avg Carbohydrates | 43.36      | 41.49     |
| Avg Protein       | 20.78      | 11.47     |

#### Key Findings

* Starbucks food products contained fewer calories.
* Starbucks food products contained lower fat levels.
* McDonald's food products provided significantly higher protein content.
* Fiber values were relatively similar across both brands.

---

### Overall Brand Comparison

| Metric       | McDonald's | Starbucks |
| ------------ | ---------- | --------- |
| Avg Calories | 368.27     | 226.70    |
| Avg Fat      | 14.17      | 6.40      |
| Avg Sugars   | 29.42      | 32.96     |
| Avg Protein  | 13.34      | 7.77      |

---

## Challenges Solved

### Duplicate Data Handling

Identified and removed 22 duplicate records from the Starbucks drinks dataset to prevent biased nutritional calculations.

### Missing Value Management

Handled missing nutritional attributes while preserving data integrity and avoiding artificial data imputation.

### Schema Integration

Designed and implemented a common schema capable of integrating four heterogeneous datasets.

### Data Standardization

Resolved inconsistent column names, formats, and attribute structures across multiple sources.

### Fair Comparison Design

Separated food and beverage analyses to avoid misleading conclusions and improve analytical validity.

---

## Business Insights

The analysis demonstrates that nutritional comparisons cannot rely on a single metric.

Key observations:

* Starbucks generally performed better for calorie control and sodium reduction.
* Starbucks beverages showed lower sugar levels than McDonald's beverages.
* McDonald's food products offered higher protein content.
* Different nutritional priorities lead to different conclusions regarding healthiness.

This highlights the importance of evaluating multiple nutritional dimensions simultaneously.

---

## Sample Outputs

The project generated multiple analytical outputs including:

* Dataset profiling results
* Duplicate analysis reports
* Missing value assessments
* Nutritional aggregation reports
* Brand-level comparisons
* Food versus beverage analysis
* Overall nutritional evaluations

Screenshots of selected outputs are available in the **screenshots** folder.

---

## Repository Structure

```text
McDonalds-Starbucks-Nutrition-Analysis
│
├── data/
│   └── Dataset descriptions and metadata
│
├── notebooks/
│   └── Nutritional_Snack_analysis.ipynb
│
├── reports/
│   ├── Analysis_Report.pdf
│   └── Analysis_Report.docx
│
├── screenshots/
│   └── Output screenshots
│
└── README.md
```

---

## Key Skills Demonstrated

* PySpark DataFrames
* Data Profiling
* Data Cleaning
* Missing Value Handling
* Duplicate Detection
* Schema Standardization
* Dataset Integration
* Exploratory Data Analysis
* Data Aggregation
* Business Reporting
* Data Quality Assessment
* Analytical Problem Solving

---

## Author

### Viswanadh.G

Data Engineering Enthusiast with hands-on experience in SQL, Python, PySpark, Azure Data Factory, Azure SQL Database, Azure Synapse Analytics, ETL pipelines, data cleaning, and analytical reporting.
