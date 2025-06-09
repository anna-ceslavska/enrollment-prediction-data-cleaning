# Enrollment Data Cleaning & Feature Engineering (R)

This project focuses on preparing a real-world admissions dataset for predictive modeling, with an emphasis on data cleaning, feature engineering, and transformation. The dataset includes over 18,000 records and 34 features, extracted from the SQL-based Slate CRM platform used by college admissions teams.

---

## Project Overview

The original dataset included raw, inconsistently formatted, and text-heavy features, making it unsuitable for direct modeling. Through structured cleaning and engineering, this project transformed the admissions data into a ready-to-model format, enabling exploratory data analysis (EDA) and supervised machine learning.

---

## Files

- `data_cleaning_engineering.qmd` — Main Quarto notebook for all cleaning, engineering, and visualization steps
- `enrollment.xlsx` — Original dataset (exported from Slate)
---

## Key Techniques

### Data Cleaning
- Renamed all columns using `snake_case` for code consistency
- Dropped timestamp and high-cardinality text features (e.g., interactions, tags)
- Replaced missing values in behavioral metrics with `0` to reflect no interaction
- Split combined variables like `round` into `year` and `period`

### Feature Engineering
- Created `our_visits` to flag institutional outreach events attended
- Parsed tags to define a structured `student_group` variable (UWC, Recruit, Scholars)
- Calculated ZIP code distances using `zipcodeR` and categorized applicants into `location` (International, Domestic, IL)
- Converted engagement and email performance metrics from character to numeric
- Created a binary outcome variable `enrolling_stage` based on final admission decision

### Visualization
- Used `ggplot2` to visualize class balance between enrolled vs. not enrolled students

---

## Outcome

By the end of this process, the dataset was clean, numerically consistent, and analytically structured. It’s now ready for:
- Correlation analysis
- Logistic regression, tree-based models, and other supervised learning techniques
- Insights on geographic, behavioral, and program-driven enrollment patterns

---

## R Libraries Used

- `tidyverse`
- `janitor`
- `zipcodeR`
- `ggplot2`
- `readxl`, `writexl`
- `stringr`, `dplyr`, `here`, `skimr`

---

## Author

**Anna Ceslavska**  
Senior at Lake Forest College  
Majors: Data Science and Economics  
