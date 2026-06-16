# Dataset Overview

This project uses four nutritional datasets from McDonald's and Starbucks.

## Source Datasets

### 1. mcd.csv
- Brand: McDonald's
- Records: 260
- Description: Nutritional information for McDonald's food and beverage products.
- Attributes include Calories, Fat, Carbohydrates, Fiber, Protein, Sugars and Sodium.

### 2. sb_drinks.csv
- Brand: Starbucks
- Original Records: 177
- Duplicate Records Removed: 22
- Final Records Used: 155
- Description: Starbucks beverage nutritional information.

### 3. sb_drink_expanded.csv
- Brand: Starbucks
- Records: 242
- Description: Expanded Starbucks beverage dataset containing detailed nutritional attributes including caffeine information.

### 4. sb_food.csv
- Brand: Starbucks
- Records: 113
- Description: Nutritional information for Starbucks food products.

## Final Integrated Dataset

After cleaning, standardization, and schema integration:

- McDonald's Records: 260
- Starbucks Records: 510
- Total Records: 770

## Data Quality Issues Addressed

- 22 duplicate records identified and removed from sb_drinks.csv
- Missing caffeine values identified
- Placeholder "-" values converted to NULL
- Mixed caffeine values such as "Varies" and "varies" preserved
- Common schema created across all datasets

## Common Schema

The datasets were standardized into a unified schema containing:

- Brand
- Source_File
- Category
- Item_Name
- Calories
- Fat
- Carbohydrates
- Fiber
- Sugars
- Protein
- Sodium
- Caffeine
