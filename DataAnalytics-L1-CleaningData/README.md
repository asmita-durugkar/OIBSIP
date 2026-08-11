# Cleaning Data 🧹

## Overview
This project is part of the **Oasis Infobyte Data Analytics Internship (Level 1 - Task 3)**. The primary objective of this task is to process and clean a raw dataset, transforming it into a high-quality, structured format ready for exploratory data analysis (EDA) and predictive modeling.

## Project Workflow
1. **Data Inspection:** Loaded the raw dataset and examined its structure, data types, and initial rows to understand the scope of the messiness.
2. **Handling Missing Values:** Identified null/NaN values across columns and applied appropriate imputation techniques (e.g., filling with mean/median for numerical data, mode for categorical data) or dropped unrecoverable records.
3. **Removing Duplicates:** Checked for and eliminated duplicate rows to ensure data integrity and prevent skewed analysis.
4. **Outlier Treatment:** Utilized statistical methods and visualizations (such as boxplots) to detect anomalies and handle extreme outliers appropriately.
5. **Standardization & Formatting:** Corrected inconsistent data entries, standardized text cases (e.g., stripping whitespace, converting to lowercase), and converted columns to their proper data types (e.g., parsing strings into DateTime objects).

## Technologies Used
* **Language:** Python
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn
* **Environment:** Google Colab / Jupyter Notebook

## How to Run
1. Clone this repository to your local machine.
2. Open `Data_cleaning.ipynb` in Jupyter Notebook or Google Colab.
3. Ensure the raw dataset is uploaded or correctly linked in the notebook.
4. Run all cells sequentially to view the step-by-step data cleaning process.
