# Data Cleaning & Preprocessing: Cafe Sales 

This repository contains the solution for the **Data Analytics Level 1 - Cleaning Data** task. The objective of this project is to transform a raw, unstructured dataset into a high-quality, standardized format suitable for exploratory data analysis (EDA).

## 📊 Dataset
The project utilizes the [Cafe Sales Dirty Data for Cleaning Training](https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training) dataset from Kaggle. It represents retail cafe transactions injected with various intentional anomalies, such as missing values, inconsistent data types, and text formatting errors.

## 🧹 Cleaning Workflow & Strategies
The following operations were performed using **Python (Pandas, NumPy)**:

1. **Data Quality Profiling:** Generated an initial report mapping out null counts, duplicates, and data type mismatches across all 10,000 rows.
2. **Missing Data Handling:**
   * Standardized text anomalies (`"ERROR"`, `"UNKNOWN"`) into true `NaN` values.
   * Addressed numeric gaps by imputing missing `Quantity` and `Price Per Unit` with column means.
   * Recalculated missing `Total Spent` fields using the mathematical relationship: `Quantity * Price Per Unit`.
   * Logically deduced missing `Item` names where a unique `Price Per Unit` served as an identifier (e.g., $3.0 = Cake).
   * Filled remaining unresolvable categorical gaps (`Location`, `Payment Method`) with `"UNKNOWN"` to preserve row integrity and total revenue counts.
3. **Data Type Correction:** Converted `Transaction Date` to proper `datetime` objects and explicitly cast IDs and categorical features to strings.
4. **Outlier Detection:** Utilized the IQR (Interquartile Range) method and Seaborn boxplots to analyze `Total Spent`. Legitimate high-value transactions (e.g., $25.0) were retained to prevent data loss on valid VIP purchases.

## 📈 Results: Before vs. After
| Metric | Before Cleaning | After Cleaning |
| :--- | :--- | :--- |
| **Total Rows** | 10,000 | 10,000 |
| **Duplicate Rows** | 0 | 0 |
| **Total Missing Values** | 6,826 | 460 |

*Note: Remaining missing values represent unresolvable categorical data intentionally preserved to maintain transaction volume accuracy.*

## 🛠️ Technologies Used
* **Python 3**
* **Pandas & NumPy:** Data Manipulation and Mathematical Imputation
* **Matplotlib & Seaborn:** Outlier Visualization 
* **Google Colab:** Development Environment

## 🚀 How to Run
1. Clone the repository.
2. Ensure you have the required libraries installed (`pip install pandas numpy matplotlib seaborn`).
3. Run the Jupyter Notebook to view the step-by-step data cleaning pipeline and generate the final `cleaned_sales.csv` file.
